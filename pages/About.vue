<template>
  <div class="container about text-left">
    <section id="about" class="about">
      <div class="">
        <div class="section-title text-left">
          <h2 class="text-center">Reihan Andhika Putra</h2>
          <h3>About</h3>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore
              magna aliqua.Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore
              magna aliqua.</p>
        </div>
        <div class="row">
          <div class="col-lg-4" >
            <img src="~/assets/images/Foto_13519043_Reihan Andhika P.jpg" class="" alt="" width="300">
          </div>
          <div class="col-lg-8 pt-0 mt-0 content" >
            <h3>Web Developer</h3>
            <p class="font-italic">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore
              magna aliqua.
            </p>
            <div class="row">
              <div class="col-lg-6">
                <ul>
                  <li><i class="icofont-rounded-right"></i> <strong>Birthday:</strong> 2 May 2001</li>
                  <li><i class="icofont-rounded-right"></i> <strong>Website:</strong> www.example.com</li>
                  <li><i class="icofont-rounded-right"></i> <strong>Phone:</strong> +123 456 7890</li>
                  <li><i class="icofont-rounded-right"></i> <strong>City:</strong> City : New York, USA</li>
                </ul>
              </div>
              <div class="col-lg-6">
                <ul>
                  <li><i class="icofont-rounded-right"></i> <strong>Age:</strong> 30</li>
                  <li><i class="icofont-rounded-right"></i> <strong>Degree:</strong> Master</li>
                  <li><i class="icofont-rounded-right"></i> <strong>PhEmailone:</strong> email@example.com</li>
                  <li><i class="icofont-rounded-right"></i> <strong>Freelance:</strong> Available</li>
                </ul>
              </div>
            </div>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore
              magna aliqua.Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore
              magna aliqua.
            </p>
          </div>
        </div>

      </div>
    </section><!-- End About Section -->
  </div>
</template>

<style scoped>
.about .content h3 {
  font-weight: 700;
  font-size: 26px;
  color: #173b6c;
}

.about .content ul {
  list-style: none;
  padding: 0;
}

.about .content ul li {
  padding-bottom: 10px;
}

.about .content ul i {
  font-size: 20px;
  padding-right: 2px;
  color: #42b883;
}

.about .content p:last-child {
  margin-bottom: 0;
}

section {
  padding: 10px 0;
  overflow: hidden;
}

.section-bg {
  background: #f5f8fd;
}

.section-title {
  padding-bottom: 10px;
  margin-bottom: 20px;
}

.section-title h2 {
  font-size: 32px;
  font-weight: bold;
  margin-bottom: 0px;
  padding-bottom: 0px;
  position: relative;
  color: #173b6c;
}
.section-title h3 {
  font-size: 32px;
  font-weight: bold;
  margin-bottom: 10px;
  padding-bottom: 10px;
  position: relative;
  color: #173b6c;
}


.section-title h3::after {
  content: '';
  position: absolute;
  display: block;
  width: 100px;
  height: 3px;
  background: #42b883;
  bottom: 0;
  left: 0;
}
.section-title h2::before {
  background: #ffffff;
  
}
.section-title p {
  margin-bottom: 0;
}
</style>
