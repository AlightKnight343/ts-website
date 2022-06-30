<svelte:head>
    <title>Tech Syndicate | Achievements</title>
</svelte:head>

<script>
    // import achievements from '../../data/achievements.json'
    import {onMount} from 'svelte';
    onMount(()=>{

        document.getElementById('21').style.display = 'none';
        document.getElementById('20').style.display = 'none';
        document.getElementById('19').style.display = 'none';

        document.getElementById('2022').addEventListener('click', ()=>{
            document.getElementById('22').style.display = 'block';
            document.getElementById('21').style.display = 'none';
            document.getElementById('20').style.display = 'none';
            document.getElementById('19').style.display = 'none';
            document.getElementById('2022').classList.add('active');
            document.getElementById('2021').classList.remove('active');
            document.getElementById('2020').classList.remove('active');
            document.getElementById('2019').classList.remove('active');
        });

        document.getElementById('2021').addEventListener('click', ()=>{
            document.getElementById('22').style.display = 'none';
            document.getElementById('21').style.display = 'block';
            document.getElementById('20').style.display = 'none';
            document.getElementById('19').style.display = 'none';
            document.getElementById('2022').classList.remove('active');
            document.getElementById('2021').classList.add('active');
            document.getElementById('2020').classList.remove('active');
            document.getElementById('2019').classList.remove('active');
        });


        document.getElementById('2020').addEventListener('click', ()=>{
            document.getElementById('22').style.display = 'none';
            document.getElementById('21').style.display = 'none';
            document.getElementById('20').style.display = 'block';
            document.getElementById('19').style.display = 'none';
            document.getElementById('2022').classList.remove('active');
            document.getElementById('2021').classList.remove('active');
            document.getElementById('2020').classList.add('active');
            document.getElementById('2019').classList.remove('active');
        });


        document.getElementById('2019').addEventListener('click', ()=>{
            document.getElementById('22').style.display = 'none';
            document.getElementById('21').style.display = 'none';
            document.getElementById('20').style.display = 'none';
            document.getElementById('19').style.display = 'block';
            document.getElementById('2022').classList.remove('active');
            document.getElementById('2021').classList.remove('active');
            document.getElementById('2020').classList.remove('active');
            document.getElementById('2019').classList.add('active');
        });


    })
    let achievements = [
        [
        {event: "EXUN", school: "DPS RK Puram", position:"Winners"},
        {event: "CORE", school: "DPS RK Puram", position:"Runners Up"}
        ],
        [
        {event: "Code Wars", school: "DPS RK Puram", position:"Fourth"},
        {event: "Minet", school: "DPS RK Puram", position:"Winners"},
        ],
        [
        {event: "Robotronics", school: "Amity 46", position:"Runners Up"},
        {event: "nCrypt", school: "DPS RK Puram", position:"Winners"},
        ],
        [
        {event: "Binary Bots", school: "Lotus Valley", position:"Winners"},
        {event: "EXUN", school: "DPS RK Puram", position:"Second Runners Up"},
        ]
    ]
    let achievements22 = achievements[0]
    let achievements21 = achievements[1]
    let achievements20 = achievements[2]
    let achievements19 = achievements[3]
</script>


<main>
	<h1>Achievements</h1>
	<div class="year-wrapper">
		<div id="2022" class="year active">2022</div>
		<div id="2021" class="year">2021</div>
		<div id="2020" class="year">2020</div>
		<div id="2019" class="year">2019</div>
	</div>

	<div class="event-wrapper" id="22">
        {#each achievements22 as achievement}
		<div class="event">
			<div class="position"></div>
			<h2>{achievement.event}</h2>
            <p class="text">By {achievement.school} <br> Overall Position: <span>{achievement.position}</span></p>
            <p class="details-toggle">Details</p>
		</div>
        {/each}
	</div>
	<div class="event-wrapper" id="21">
        {#each achievements21 as achievement}
		<div class="event">
			<div class="position"></div>
			<h2>{achievement.event}</h2>
            <p class="text">By {achievement.school} <br> Overall Position: <span>{achievement.position}</span></p>
            <p class="details-toggle">Details</p>
	</div>
    {/each}
	<div class="event-wrapper" id="20">
        {#each achievements20 as achievement}
		<div class="event">
			<div class="position"></div>
			<h2>{achievement.event}</h2>
            <p class="text">By {achievement.school} <br> Overall Position: <span>{achievement.position}</span></p>
            <p class="details-toggle">Details</p>
		</div>
        {/each}
        <div class="event-wrapper" id="19">
        {#each achievements19 as achievement}
		<div class="event">
			<div class="position"></div>
			<h2>{achievement.event}</h2>
            <p class="text">By {achievement.school} <br> Overall Position: <span>{achievement.position}</span></p>
            <p class="details-toggle">Details</p>
		</div>
        {/each}

</main>

<style>
	h1 {
		color: #fff;
		font-size: 3.5vw;
		margin-left: 5vw;
		font-weight: bold;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}

    .year-wrapper, .event-wrapper{
        margin-left: 5vw;
    }

    .event-wrapper{
        margin-top: 10vw;
    }

    .year{
        background: #171717;
        width: 7.5vw;
        display:flex;
        height: 3vw;
        border-radius: 7.5px;
        color: #fff;
        font-size: 1.5rem;
        text-align: center;
        align-items: center;
        justify-content: center;
        float: left;
        margin-right: 1.25vw;
        cursor: pointer
    }

    .event{
        width: 27.5vw;
        height: 15vw;
        background: #171717;
        border-radius: 7.5px;
        margin-bottom: 2.5vw;
        float: left;
        margin-right: 3vw;
    }

    .position{
        width: 22px;
        height: 22px;
        border-radius: 50%;
        background-color: #fff;
        margin-top: 3vw;
        margin-left: 2vw;
        display:inline-block;
    }

    .event h2{
        display: inline;
        color: #16e16e;
        margin-left: 1vw;
        font-size: 2rem;
    }

    .text{
        margin-left: 4.7vw;
        color: rgb(160, 160, 160);
        font-size: 1.2rem;
    }

    .text span{
        color: #d6d6d6;
        font-weight: 500;
    }

    .details-toggle{
        margin-left: 4.7vw;
        color: #fff;
        font-weight: 600;
        font-size: 1.2rem;
    }

    .active{color: #16e16e;}

</style>
