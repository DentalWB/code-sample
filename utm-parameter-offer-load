window.addEventListener('load', function () {
  
    function getUrlParameter(name) {
      name = name.replace(/[\[]/, '\\[').replace(/[\]]/, '\\]');
      var regex = new RegExp('[\\?&]' + name + '=([^&#]*)');
      var results = regex.exec(location.search);
      return results === null ? '' : decodeURIComponent(results[1].replace(/\+/g, ' '));
    };
  
    const offerUtm = getUrlParameter('utm_content');

    $('.offer-1').addClass('hide')
    $('.offer-2').addClass('hide')
    $('.offer-3').addClass('hide')
  
   if (offerUtm == 'offer-2') {
      $('.offer-2').removeClass('hide')
    } else if (offerUtm == 'offer-3') {
      $('.offer-3').removeClass('hide')
    } else {
      $('.offer-1').removeClass('hide')
    }
  });
