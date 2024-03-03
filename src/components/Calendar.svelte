<!-- Credits to vkurko/calendar -->
<script>
	import Todos from "../components/Todos.svelte";
    import Calendar from '@event-calendar/core';
    import TimeGrid from '@event-calendar/time-grid';

    let plugins = [TimeGrid];
    let options = {
        view: 'timeGridWeek',
        events: [
            // your list of events
        ]
    };
</script>

<div class="calendar-wrapper">
	<Todos />
	<div class="calendar">
		<Calendar {plugins} {options} />
	</div>
</div>

<style>
	.calendar-wrapper{
		display: flex;
		justify-content: center;
		justify-items: center;
		gap: 50px;

	}
	
	.calendar {
		margin: 2rem 0 4rem 0;
		padding: 1rem;
		position: relative;
		box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.2), 0 2.5rem 5rem 0 rgba(0, 0, 0, 0.1);flex-direction: column;
	}
</style>