window.onload = function () {
  var gotoFull = document.getElementsByClassName('full')[0];
  gotoFull.addEventListener('click',function (){
    window.top.location.href = 'https://codepen.io/loerm/pen/oNBMXxR';
  });
  var figure = document.querySelectorAll('figure');
  // console.log(figure);
  
  function findXY_WH (e,that) {
    var m_posx = 0, m_posy = 0, e_posx = 0, e_posy = 0,
           obj = that;
    //get mouse position on document crossbrowser
    if (!e){e = window.event;}
    if (e.pageX || e.pageY){
        m_posx = e.pageX;
        m_posy = e.pageY;
    } else if (e.clientX || e.clientY){
        m_posx = e.clientX + document.body.scrollLeft
                 + document.documentElement.scrollLeft;
        m_posy = e.clientY + document.body.scrollTop
                 + document.documentElement.scrollTop;
    }
    //get parent element position in document
    if (obj.offsetParent){
        do { 
            e_posx += obj.offsetLeft;
            e_posy += obj.offsetTop;
        } while (obj = obj.offsetParent);
    }
    // mouse position minus elm position is mouseposition relative to element:
    let xFind = (m_posx-e_posx),
        yFind = (m_posy-e_posy),
        wFind = that.offsetWidth,
        hFind = that.offsetHeight;
    return [(xFind < 1) ? 1 : xFind, (yFind < 1) ? 1 : yFind, wFind, hFind];
  } 

  figure.forEach( item => {
    item.addEventListener('mouseenter', function (e) {
      let [x, y, w, h] = findXY_WH(e,this);
      y = (y >= h) ? --h : y;
      let ratio = w/h;
      let obj = this;
      
      let ani = '';
      
      if (x/y < ratio && x/(h-y) < ratio){
         ani = 'left';
      } else if (x/y > ratio && x/(h-y) > ratio){
        ani = 'right';
      } else if (x/y >= ratio && x/(h-y) <= ratio){
        ani = 'top';
      } else if (x/y <= ratio && x/(h-y) >= ratio){
        ani = 'bot';
      }
      
      if (ani == 'left') {
        setTimeout(function () {
          obj.children[1].style.transition = '.3s ease';
          obj.children[1].style.left = '0';
          obj.children[1].style.top = '0';
        },0);
        obj.children[1].style.transition = 'none';
        obj.children[1].style.left = '-100%';
        obj.children[1].style.top = '0';
      }
      else if (ani == 'right') {
        setTimeout(function () {
          obj.children[1].style.transition = '.3s ease';
          obj.children[1].style.left = '0';
          obj.children[1].style.top = '0';
        },0);
        obj.children[1].style.transition = 'none';
        obj.children[1].style.left = '100%';
        obj.children[1].style.top = '0';
      }
      else if (ani == 'top') {
        setTimeout(function () {
          obj.children[1].style.transition = '.3s ease';
          obj.children[1].style.left = '0';
          obj.children[1].style.top = '0';
        },0);
        obj.children[1].style.transition = 'none';
        obj.children[1].style.left = '0';
        obj.children[1].style.top = '-100%';
      }
      else if (ani == 'bot') {
        setTimeout(function () {
          obj.children[1].style.transition = '.3s ease';
          obj.children[1].style.left = '0';
          obj.children[1].style.top = '0';
        },0);
        obj.children[1].style.transition = 'none';
        obj.children[1].style.left = '0';
        obj.children[1].style.top = '100%';
      }
    });
    item.addEventListener('mouseleave', function (e) {
      let [x, y, w, h] = findXY_WH(e,this);
      y = (y >= h) ? --h : y;
      let ratio = w/h;
      let obj = this;
      
      let ani = '';
      
      if (x/y < ratio && x/(h-y) < ratio){
         ani = 'Oleft';
      } else if (x/y > ratio && x/(h-y) > ratio){
        ani = 'Oright';
      } else if (x/y >= ratio && x/(h-y) <= ratio){
        ani = 'Otop';
      } else if (x/y <= ratio && x/(h-y) >= ratio){
        ani = 'Obot';
      }
      
      if (ani == 'Oleft') {
        setTimeout(function () {
          obj.children[1].style.left = '-100%';
          obj.children[1].style.top = '0';
        },0);
      }
      else if (ani == 'Oright') {
        setTimeout(function () {
          obj.children[1].style.left = '100%';
          obj.children[1].style.top = '0';
        },0);
      }
      else if (ani == 'Otop') {
        setTimeout(function () {
          obj.children[1].style.left = '0';
          obj.children[1].style.top = '-100%';
        },0);
      }
      else if (ani == 'Obot') {
        setTimeout(function () {
          obj.children[1].style.left = '0';
          obj.children[1].style.top = '100%';
        },0);
      }
      
      console.log(ani,x,y,w,h)
    });
  })
}
