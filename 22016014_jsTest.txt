$(function() {  
$('button').click(function(){
    alert("없지롱");
  });
});

// 여기부터 ▼▼▼▼▼
var items = [
  {
      profile : 'https://source.unsplash.com/random',
      feedimage : 'https://source.unsplash.com/random',
      name : 'first-user',
      title : '1번째 게시글',
      content : 'Think of me',
      btn : 'View Detail'
  },
  {
      profile : 'https://source.unsplash.com/random',
      feedimage : 'https://source.unsplash.com/random',
      name : 'second-user',
      title : '2번째 게시글',
      content : 'If I fall in love',
      btn : 'View Detail'
  },
  {
      profile : 'https://source.unsplash.com/random',
      feedimage : 'https://source.unsplash.com/random',
      name : 'third-user',
      title : '3번째 게시글',
      content : 'Always be with you',
      btn : 'View Detail'
  }
];

var container = $('.section');

$.each(items , function(i){
  container.append('<div class="nameBar">' + 
      '<div class="profile">' + this.profile + '</div>' + 
      '<div  class="user-id">' + this.name + '</div>'  + '</div>' +
      '<div class="feedBox">' + '<div class="feedImg">' + this.feedimage + '</div>' + 
      '<div class="text">' + '<h3>' + this.title + '</h3>' + '<p>' + this.content + '</p>' + 
      '<button class="btn">' + this.btn + '</button>' + '</div>' + '</div>');
})