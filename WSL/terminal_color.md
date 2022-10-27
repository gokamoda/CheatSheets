<style>
* {
margin: 0;
padding: 0;
box-sizing: content-box;
}

.dark {
background-color: #1E1E1E;
height: 500px;
color: white;
}

.light {
background-color: #E1E1E1;
height: 500px;
color: black;
}

.background {
display: table;
height: 100px;
width: 100%
}

body {
/* background-color: #1E1E1E; */
color: white
}

.boxes {
width: 600px;
margin: 0 auto;
display: flex;
flex-wrap: wrap;
}

.box {
width: 150px;
height: 150px;
display: table;
text-align: center;
vertical-align: middle;
}

.dark-label {
width: 100%;
height: 100%;
display: table;
text-align: center;
vertical-align: middle;
}

.light-label {
width: 100%;
height: 100%;
display: table;
text-align: center;
vertical-align: middle;
}

p {
display: table-cell;
vertical-align: middle;
font-family: Arial;
}


.black {
background-color: #000000;
}

.white {
background-color: #AAAAAA;
}

.red {
background-color: #99000D;
}

.green {
background-color: #0D9900;
}

.blue {
background-color: #005999;
}

.cyan {
background-color: #0F9992;
}

.purple {
background-color: #8C0099;
}

.yellow {
background-color: #99920F;
}

.b-black {
background-color: #555555;
}

.b-white {
background-color: #FFFFFF;
}

.b-red {
background-color: #CC0011;
}

.b-green {
background-color: #11CC00;
}

.b-purple {
background-color: #BB00CC;
}

.b-yellow {
background-color: #CCC314;
}

.b-blue {
background-color: #0077CC;
}

.b-cyan {
background-color: #14CCC3;
}

.text-black {
color: #000000;
}

.text-white {
color: #AAAAAA;
}

.text-red {
color: #99000D;
}

.text-green {
color: #0D9900;
}

.text-blue {
color: #005999;
}

.text-cyan {
color: #0F9992;
}

.text-purple {
color: #8C0099;
}

.text-yellow {
color: #99920F;
}


.text-b-black {
color: #555555;
}

.text-b-white {
color: #FFFFFF;
}

.text-b-red {
color: #CC0011;
}

.text-b-green {
color: #11CC00;
}

.text-b-purple {
color: #BB00CC;
}

.text-b-yellow {
color: #CCC314;
}

.text-b-blue {
color: #0077CC;
}

.text-b-cyan {
color: #14CCC3;
}
</style>

<div class="dark">
<div class="background">
<div class="dark-label">
  <p>#1E1E1E</p>
</div>
</div>
<div class="boxes">
<div class="box black">
  <p>
    Black<br>
    \[\033[00;30m\]<br>
    #000000
  </p>
</div>

<div class="box purple">
  <p>
    Pruple<br>
    \[\033[00;35m\]<br>
    #8C0099
  </p>
</div>

<div class="box red">
  <p>
    Red<br>
    \[\033[00;31m\]<br>
    #99000D
  </p>
</div>

<div class="box yellow">
  <p>
    Yellow<br>
    \[\033[00;33m\]<br>
    #99920F
  </p>
</div>

<div class="box white">
  <p>
    White<br>
    \[\033[00;37m\]<br>
    #AAAAAA
  </p>
</div>

<div class="box blue">
  <p>
    Blue<br>
    \[\033[00;34m\]<br>
    #005999
  </p>
</div>

<div class="box cyan">
  <p>
    Cyan<br>
    \[\033[00;36m\]<br>
    #0F9992
  </p>
</div>

<div class="box green">
  <p>
    Green<br>
    \[\033[00;32m\]<br>
    #0D9900
  </p>
</div>
</div>
<div class="background">
<div class="dark-label">
  <p>
    <span class="text-black">black</span>
    <span class="text-purple">purple</span>
    <span class="text-red">red</span>
    <span class="text-yellow">yellow</span>
    <span class="text-white">white</span>
    <span class="text-blue">blue</span>
    <span class="text-cyan">cyan</span>
    <span class="text-green">green</span><br>
    <span class="text-b-black">black</span>
    <span class="text-b-purple">purple</span>
    <span class="text-b-red">red</span>
    <span class="text-b-yellow">yellow</span>
    <span class="text-b-white">white</span>
    <span class="text-b-blue">blue</span>
    <span class="text-b-cyan">cyan</span>
    <span class="text-b-green">green</span>
  </p>
</div>
</div>

<div class="light">
<div class="background">
  <div class="light-label">
    <p>#E1E1E1</p>
  </div>
</div>
<div class="boxes">
  <div class="box b-black">
    <p>
      Bright Black<br>
      \[\033[01;30m\]<br>
      #555555
    </p>
  </div>

  <div class="box b-purple">
    <p>
      Bright Purple<br>
      \[\033[01;35m\]<br>
      #BB00CC
    </p>
  </div>

  <div class="box b-red">
    <p>
      Bright Red<br>
      \[\033[01;31m\]<br>
      #CC0011
    </p>
  </div>

  <div class="box b-yellow">
    <p>
      Bright Yellow<br>
      \[\033[01;33m\]<br>
      #CCC314
    </p>
  </div>

  <div class="box b-white">
    <p>
      Bright White<br>
      \[\033[01;37m\]<br>
      #FFFFFF
    </p>
  </div>

  <div class="box b-blue">
    <p>
      Bright Blue<br>
      \[\033[01;34m\]<br>
      #0077CC
    </p>
  </div>

  <div class="box b-cyan">
    <p>
      Bright Cyan<br>
      \[\033[01;36m\]<br>
      #14CCC3
    </p>
  </div>

  <div class="box b-green">
    <p>
      Bright Green<br>
      \[\033[01;32m\]<br>
      #11CC00
    </p>
  </div>






</div>
<div class="background">
  <div class="light-label">
    <p>
      <span class="text-black">black</span>
      <span class="text-purple">purple</span>
      <span class="text-red">red</span>
      <span class="text-yellow">yellow</span>
      <span class="text-white">white</span>
      <span class="text-blue">blue</span>
      <span class="text-cyan">cyan</span>
      <span class="text-green">green</span><br>
      <span class="text-b-black">black</span>
      <span class="text-b-purple">purple</span>
      <span class="text-b-red">red</span>
      <span class="text-b-yellow">yellow</span>
      <span class="text-b-white">white</span>
      <span class="text-b-blue">blue</span>
      <span class="text-b-cyan">cyan</span>
      <span class="text-b-green">green</span>
    </p>
  </div>
</div>
</div>
