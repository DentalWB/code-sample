document.addEventListener('DOMContentLoaded', function(event) {
    function getTimeRemainingMisenClockJustuno(endtime) {
      const total = Date.parse(endtime) - Date.parse(new Date());
      const seconds = Math.floor((total / 1000) % 60);
      const minutes = Math.floor((total / 1000 / 60) % 60);
      const hours = Math.floor((total / (1000 * 60 * 60)) % 24);

      return {
        total,
        hours,
        minutes,
        seconds
      };
    }

    function initializeClockMisenClockJustuno(id, endtime, extended) {
      const clock = document.getElementById(id);
      const hoursSpan = clock.querySelector('.hours');
      const minutesSpan = clock.querySelector('.minutes');
      const secondsSpan = clock.querySelector('.seconds');
      const extendedSpan = clock.querySelector('.extended');

      function updateClockMisenClockJustuno() {
        const t = getTimeRemainingMisenClockJustuno(endtime);

        hoursSpan.innerHTML = ('0' + t.hours).slice(-2);
        minutesSpan.innerHTML = ('0' + t.minutes).slice(-2);
        secondsSpan.innerHTML = ('0' + t.seconds).slice(-2);
        if (extended === true) {
            extendedSpan.innerHTML = '<strong>EXTENDED: </strong>';
        }

        if (t.total <= 0) {
          clearInterval(timeinterval);
        }
      }

      updateClockMisenClockJustuno();
      const timeinterval = setInterval(updateClockMisenClockJustuno, 1000);
    }

    var extendedMisenClockJustuno = false;
    var currentTimeMisenClockJustuno = new Date(Date.now());
    var nextDayMisenClockJustuno = new Date(currentTimeMisenClockJustuno.setDate(currentTimeMisenClockJustuno.getDate() + 1));
    nextDayMisenClockJustuno.setHours(1);
    nextDayMisenClockJustuno.setMinutes(0);
    nextDayMisenClockJustuno.setSeconds(0);
    currentTimeMisenClockJustuno = new Date(Date.now());

    if (currentTimeMisenClockJustuno.getHours() < 1) {
        extendedMisenClockJustuno = true;
    }

    initializeClockMisenClockJustuno('MisenClockJustuno', nextDayMisenClockJustuno, extendedMisenClockJustuno);
});
