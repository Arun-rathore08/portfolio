<template>
  <div ref="home" class="min-h-screen bg-black text-white font-sans" id="home">
    <div class="container mx-auto py-10 px-5 md:px-20">
      <!-- Navbar -->
<!-- Navbar -->
        <nav :class="['fixed top-0 left-0 w-full bg-black text-white py-5 px-10 z-20 transition-all duration-300 flex justify-between items-center', navVisible || !isDesktop ? 'opacity-100' : 'opacity-0 pointer-events-none']">
          <nuxt-link to="/">
            <img src="/logo.png" style="width: 75px;" alt="Logo">
          </nuxt-link>
          <!-- Sidebar Toggle Button for Mobile (Always visible) -->
          <button class="text-white md:hidden" @click="toggleSidebar">
            <!-- Toggle Menu Icon -->
            <svg v-if="!sidebarVisible" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-6 h-6">
              <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16m-7 6h7" />
            </svg>
            <!-- Close Icon -->
            <svg v-else xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-6 h-6">
              <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
          <!-- Navbar Links for Desktop -->
          <ul class="hidden md:flex justify-end space-x-8 pt-2 text-lg">
            <li><NuxtLink to="/" class="hover:text-blue-400" @click="scrollToTop">Home</NuxtLink></li>
            <li><NuxtLink to="/#about" class="hover:text-blue-400">About</NuxtLink></li>
            <li><NuxtLink to="/#work" class="hover:text-blue-400">Work</NuxtLink></li>
            <li><NuxtLink to="/#service" class="hover:text-blue-400">Services</NuxtLink></li>
            <li><NuxtLink to="/#contact" class="hover:text-blue-400">Contact</NuxtLink></li>
          </ul>
        </nav>


      <!-- Sidebar for Mobile -->
      <div :class="['fixed top-20 left-0 h-full w-42 bg-black z-30 transition-transform duration-300', sidebarVisible ? 'translate-x-0' : '-translate-x-full']">
        <nav class="flex flex-col items-center space-y-6 mt-10 text-lg text-white">
          <li :class="{ active: currentSection === 'home' }">
            <NuxtLink to="/#home" class="hover:text-blue-400" @click="toggleSidebar, scrollToSection('home')">Home</NuxtLink>
          </li>
          <li :class="{ active: currentSection === 'about' }">
            <NuxtLink to="/#about" class="hover:text-blue-400" @click="toggleSidebar, scrollToSection('about')">About</NuxtLink>
          </li>
          <li :class="{ active: currentSection === 'work' }">
            <NuxtLink to="/#work" class="hover:text-blue-400" @click="toggleSidebar, scrollToSection('work')">Work</NuxtLink>
          </li>
          <li :class="{ active: currentSection === 'service' }">
            <NuxtLink to="/#service" class="hover:text-blue-400" @click="toggleSidebar, scrollToSection('service')">Services</NuxtLink>
          </li>
          <li :class="{ active: currentSection === 'contact' }">
            <NuxtLink to="/#contact" class="hover:text-blue-400" @click="toggleSidebar, scrollToSection('contact')">Contact</NuxtLink>
          </li>
        </nav>
  </div>



      <!-- Content Section -->
      <div class="cont mt-20 ml-20">
        <!-- Hero Section -->
        <section class="flex flex-col md:flex-row items-center justify-between py-20">
          <!-- Text Section -->
          <div class="md:w-1/2">
            <h2 class="text-gray-500 text-xl">Software Developer</h2>
            <h1 class="text-6xl font-extrabold">
              Hello, I am <br />
              <span class="text-green-400">Arun Rathore</span>
            </h1>
            <p class="text-gray-400 mt-4">
              I excel at crafting elegant digital experiences and am proficient in various programming languages and technologies.
            </p>
            <div class="mt-8 flex items-center space-x-4 md:mb-0 mb-12">
              <a href="/Resume.pdf" download class="bg-green-400 text-black px-6 py-3 rounded-full">
                Download CV
              </a>
            </div>
          </div>
          <!-- Image Section -->
          <div class="relative flex justify-center items-center md:w-1/2 mt-8 md:mt-0">
            <img src="/ar.jpg" alt="Profile" class="w-64 h-64 rounded-full object-cover z-10" />
            <div class="absolute inset-0 flex justify-center items-center">
              <div v-for="n in 12" :key="n" :style="{ transform: `rotate(${n * 30}deg)` }" class="absolute">
                <div class="w-4 h-4 bg-green-400 rounded-full animate-spin-vertical"></div>
              </div>
            </div>
          </div>
        </section>
      
      <div class="container mx-auto py-32 px-5">
        <!-- Experience Section -->
        <section class="text-center py-5">
          <div class="relative flex flex-wrap justify-center space-x-4 sm:space-x-6 md:space-x-10 text-2xl">
            <div class="w-full sm:w-auto">
              <p class="font-bold text-white">0</p>
              <p class="text-gray-500">Years of experience</p>
            </div>
            <div class="w-full sm:w-auto">
              <p class="font-bold text-white">15</p>
              <p class="text-gray-500">Projects completed</p>
            </div>
            <div class="w-full sm:w-auto">
              <p class="font-bold text-white">6</p>
              <p class="text-gray-500">Technologies mastered</p>
            </div>
            <div class="w-full sm:w-auto">
              <p class="font-bold text-white">100</p>
              <p class="text-gray-500">Code commits</p>
            </div>
          </div>
        </section>
      
    </div><hr /><br />
      <!-- Add your content here -->
       <section ref="about"id="about">
         <h2>About Me</h2>
            <p class="p">
              Hi, I'm Arun Rathore, currently pursuing M.Tech in Computer Science. I have completed my B.Tech with a CGPA of 8.25. My passion lies in web development and learning new technologies to grow alongside others.
            </p>
          </section>
          
          <!-- Skills Section -->
          <section class="skills-section">
            <h2 class="h2">My Skills</h2>
            <ul>
              <li class="lt">Python & Django</li>
              <li class="lt">JavaScript & HTML/CSS</li>
              <li class="lt">MySQL & MongoDB</li>
              <li class="lt">Django REST Framework (DRF)</li>
              <li class="lt">Basic Java & Object-Oriented Programming</li>
            </ul>
          </section>
          
          <!-- Experience & Education Section -->
          <section class="experience-section">
            <h2 class="h2">Experience & Education</h2>
            <ul>
              <li class="lt">M.Tech in Computer Science (2023 - Present) - Sri Aurobindo Institute Of Technology, Indore</li>
              <li class="lt">B.Tech in Computer Science (2019 - 2023) - Technocrats Institute Of Technology, Bhopal</li>
              <li class="lt">TCS National Qualifier Test 2024 - Score: 63%</li>
            </ul>
          </section>

          <!-- Projects Section -->
          <section class="projects-section">
            <h2 class="h2">Projects</h2>
            <ul>
              <li class="lt">
                <strong>AI Chatbot:</strong> Built using Python, Django, and JavaScript. Automates responses based on user queries.
                <a href="https://github.com/Arun-rathore08/ChatBot" target="_blank">View on GitHub</a>
              </li>
              <li class="lt">
                <strong>ToDo List App:</strong> Task management app built with Python, Django, and Bootstrap.
                <a href="https://github.com/Arun-rathore08/TODO-Application" target="_blank">View on GitHub</a>
              </li>
            </ul>
          </section>
          
          
          
          <!-- Social Links Section -->
          <section class="social-section">
            <h2 class="h2">Connect with Me</h2>
            <div class="social-links">
              <a href="https://www.linkedin.com/in/arun-rathore-1b9228223" target="_blank">LinkedIn</a>
              <a href="https://github.com/Arun-rathore08" target="_blank">GitHub</a>
            </div>
          </section>

          <!-- Vision Section -->
          <section class="vision-section" style="margin-bottom: 3rem;">
            <h2 class="h2">My Vision</h2>
            <p class="p">
              I believe in helping others grow while learning together. I aim to contribute meaningfully through technology, problem-solving, and innovation.
            </p>
          </section>
          <br /><hr /><br />
          <!--mywork-->
          <section ref="work"id="work">
            <section class="portfolio-gallery flex flex-wrap justify-center gap-6">
              <h3 class="w-full text-center font-bold text-lg md:text-xl lg:text-2xl mb-6">My Work</h3>
              <div class="gallery grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                <!-- Project 1: AI ChatBot -->
                <div class="gallery-item p-4 bg-gray-800 rounded-lg shadow-lg">
                  <img src="/ai.png" alt="AI ChatBot" class="w-full h-40 object-cover rounded-t-lg" />
                  <h4 class="mt-4 text-xl font-bold text-green-400">AI ChatBot</h4>
                  <p class=" mt-2 text-gray-300">This AI chatbot is built using Python, Django, and JavaScript. It automates responses based on user queries, making interaction seamless.</p>
                  <ul class="mt-2 text-gray-400">
                    <li>Technologies: Python, Django, SQLite, HTML, CSS, JavaScript</li>
                    <li>Created by: Arun Rathore</li>
                  </ul>
                  <a href="https://github.com/Arun-rathore08/ChatBot" target="_blank" class="block mt-4 text-blue-500 hover:text-blue-400">View on GitHub</a>
                </div>

                <!-- Project 2: ToDo List App -->
                <div class="gallery-item p-4 bg-gray-800 rounded-lg shadow-lg">
                  <img src="/todo.png" alt="ToDo List App" class="w-full h-40 object-cover rounded-t-lg" />
                  <h4 class="mt-4 text-xl font-bold text-green-400">ToDo List App</h4>
                  <p class="mt-2 text-gray-300">A simple and effective ToDo app to manage tasks, built with Python, Django, and Bootstrap for an intuitive UI and smooth functionality.</p>
                  <ul class="mt-2 text-gray-400">
                    <li>Technologies: Python, Django, SQLite, HTML, CSS, Bootstrap</li>
                    <li>Created by: Arun Rathore</li>
                  </ul>
                  <a href="https://github.com/Arun-rathore08/TODO-Application" target="_blank" class="block mt-4 text-blue-500 hover:text-blue-400">View on GitHub</a>
                </div>

                <!-- Project 3: Hotel Management System -->
                <div class="gallery-item p-4 bg-gray-800 rounded-lg shadow-lg">
                  <img src="/hotel.png" alt="Hotel Management System" class="w-full h-40 object-cover rounded-t-lg" />
                  <h4 class="mt-4 text-xl font-bold text-green-400">Hotel Management System</h4>
                  <p class="mt-2 text-gray-300">A web-based solution for managing hotel operations, from bookings to customer handling. Built with PHP and MySQL.</p>
                  <ul class="mt-2 text-gray-400">
                    <li>Technologies: HTML, CSS, JavaScript, PHP, MySQL</li>
                    <li>Team: Arun Rathore, Roshan Nagose, Lakhan Singh</li>
                    <li>My Role: Database creation and management</li>
                  </ul>
                  <a href="https://github.com/Arun-rathore08" target="_blank" class="block mt-4 text-blue-500 hover:text-blue-400">View on GitHub</a>
                </div>
              </div>
            </section>
          </section>
          <br /><hr />
          <section ref="service" id="service">
            <h1>Services I Offer</h1>
            <div class="services-grid">
              <!-- Service 1: Full-stack Development -->
              <div class="service-item">
                <img src="/fullstack.png" alt="Full-stack Development" />
                <h3>Full-stack Development</h3>
                <p>I specialize in building robust full-stack solutions using cutting-edge frameworks. From frontend to backend, I ensure seamless integration for web applications.</p>
                <ul>
                  <li>Technologies: Python, Django, JavaScript, MySQL</li>
                </ul>
              </div>
              
              <!-- Service 2: Frontend Design -->
              <div class="service-item">
                <img src="/frontend.png" alt="Frontend Design" />
                <h3>Frontend Design</h3>
                <p>Modern and responsive UI/UX design with HTML, CSS, JavaScript, and frameworks like Nuxt.js. I focus on user-friendly and attractive designs.</p>
                <ul>
                  <li>Technologies: NuxtJs, HTML, CSS, JavaScript</li>
                </ul>
              </div>
      
              <!-- Service 3: Backend Design -->
              <div class="service-item">
                <img src="/backend.png" alt="Backend Design" />
                <h3>Backend Design</h3>
                <p>High-performance backend systems using Django and Django Rest Framework. I focus on creating secure, scalable, and maintainable APIs.</p>
                <ul>
                  <li>Technologies: Django, DRF, MySQL, MongoDB</li>
                </ul>
              </div>
              
              <!-- Service 4: Website Maintenance & Optimization -->
              <div class="service-item">
                <img src="/manage.png" alt="Website Maintenance" />
                <h3>Website Maintenance & Optimization</h3>
                <p>Regular updates, performance improvements, and security patches to ensure your website remains fast and secure over time.</p>
                <ul>
                  <li>Technologies: Bootstrap, CSS, JavaScript</li>
                </ul>
              </div>
              
              <!-- Service 5: Custom Web Applications -->
              <div class="service-item">
                <img src="/webapp.png" alt="Custom Web Applications" />
                <h3>Custom Web Applications</h3>
                <p>Tailored web applications built from scratch to meet specific business requirements using modern web frameworks.</p>
                <ul>
                  <li>Technologies: NuxtJs, Django, MySQL, MongoDB</li>
                </ul>
              </div>
              
              <!-- Service 6: API Creation -->
              <div class="service-item">
                <img src="/api.png" alt="API Creation" />
                <h3>API Creation</h3>
                <p>Custom-built RESTful APIs that enable seamless integration between systems and platforms for data exchange.</p>
                <ul>
                  <li>Technologies: Django Rest Framework (DRF), Python</li>
                </ul>
              </div>
              
              <!-- Service 7: Database Administration -->
              <div class="service-item">
                <img src="/database.png" alt="Database Administration" />
                <h3>Database Management</h3>
                <p>Efficient database management for both SQL and NoSQL databases, ensuring data integrity and security.</p>
                <ul>
                  <li>Technologies: MySQL, MongoDB</li>
                </ul>
              </div>
            </div>
          </section>
  
      <!-- Tech Tools Section -->
      <section class="tech-container">
        <h2>Technologies & Tools</h2>
        <div class="tech-grid">
          <div class="tech-item">
            <h4>FrontEnd Technologies</h4>
            <div class="img">
              <a href="https://developer.mozilla.org/en-US/docs/Web/HTML">
                <img src="/html.png" alt="HTML" />
              </a>
              <a href="https://developer.mozilla.org/en-US/docs/Web/CSS">
                <img src="/css.png" alt="CSS" />
              </a>
              <a href="https://tailwindcss.com/">
                <img src="/tailwind.png" alt="Tailwind CSS" />
              </a>
              <a href="https://nuxt.com/">
                <img src="/nuxt.png" alt="Nuxt Js">
              </a>
            </div>
          </div>
  
          <div class="tech-item">
            <h4>BackEnd Technologies</h4>
            <div class="img">
              <a href="https://www.python.org/">
                <img src="/python.png" alt="Python" />
              </a>
              <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript">
                <img src="/javascript.png" alt="JavaScript" />
              </a>
              <a href="https://www.django-rest-framework.org/">
                <img src="/drf.png" alt="Django Rest Framework" />
              </a>
            </div>
          </div>
  
          <div class="tech-item">
            <h4>Database Technologies</h4>
            <div class="img">
              <a href="https://www.mysql.com/">
                <img src="/mysql.png" alt="MySQL" />
              </a>
              <a href="https://www.mongodb.com/">
                <img src="/mongo.png" alt="MongoDB" />
              </a>
              <a href="https://www.postgresql.org/">
                <img src="/postgre.png" alt="PostgreSQL" />
              </a>
            </div>
          </div>
          
          <div class="tech-item">
            <h4>Tech Tools</h4>
            <div class="img">
              <a href="https://github.com/">
                <img src="/github.png" alt="GitHub" />
              </a>
              <a href="https://code.visualstudio.com/">
                <img src="/vscode.png" alt="VSCode" />
              </a>
              <a href="https://www.postman.com/">
                <img src="/postman.png" alt="Postman" />
              </a>
            </div>
          </div>
        </div>
       </section>
       <br /><hr /><br />
       <!--contact-->
       <section ref="contact" id="contact">
        <div class="contact-container mx-auto max-w-2xl p-6 bg-gray-800 rounded-lg shadow-lg">
          <h1 class="text-2xl font-bold text-center text-teal-400 mb-6">Contact Me</h1>
          <form @submit.prevent="submitForm" class="contact-form space-y-4">
            <div class="form-group">
              <label for="name" class="text-gray-300">Name:</label>
              <input type="text" v-model="formData.name" required placeholder="Your Name" class="w-full p-3 bg-gray-700 border border-gray-600 rounded-lg text-white"/>
            </div>
            <div class="form-group">
              <label for="email" class="text-gray-300">Email:</label>
              <input type="email" v-model="formData.email" required placeholder="Your Email" class="w-full p-3 bg-gray-700 border border-gray-600 rounded-lg text-white"/>
            </div>
            <div class="form-group">
              <label for="contact" class="text-gray-300">Contact Number:</label>
              <input type="text" v-model="formData.contact" required placeholder="Your Contact Number" class="w-full p-3 bg-gray-700 border border-gray-600 rounded-lg text-white"/>
            </div>
            <div class="form-group">
              <label for="message" class="text-gray-300">Reason for Contact:</label>
              <textarea v-model="formData.message" required placeholder="Why do you want to connect?" class="w-full p-3 bg-gray-700 border border-gray-600 rounded-lg text-white"></textarea>
            </div>
            <button type="submit" class="w-full bg-teal-500 hover:bg-teal-400 text-black font-semibold p-3 rounded-lg transition duration-300 ease-in-out">Submit</button>
            <p class="para text-teal-400 text-center mt-4" v-if="formSubmitted">Thank you! We will get back to you shortly.</p>
          </form>
        </div>

        <!-- Social links -->
        <div class="social-links flex justify-center space-x-8 mt-8">
          <a href="https://www.linkedin.com/in/arun-rathore-1b9228223" target="_blank">
            <img src="/linkedin.png" alt="LinkedIn" class="w-10 h-10">
          </a>
          <a href="https://github.com/arun-rathore08" target="_blank">
            <img src="/github.png" alt="GitHub" class="w-10 h-10">
          </a>
          <a href="mailto:15arunrathore@gmail.com">
            <img src="/gmail.png" alt="Email" class="w-10 h-10">
          </a>
        </div>
      </section>

    </div>
  </div>
  <footer class="footer flex justify-center">
      <p>© 2024 Arun Rathore. All rights reserved.</p>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  data() {
    return {
      formData: {
        name: '',
        email: '',
        contact: '',
        message: '',
      },
      formSubmitted: false,
      sidebarVisible: false,
      currentSection: 'home',
      experienceCount: 0,
      projectsCount: 0,
      technologiesCount: 0,
      commitsCount: 0,
      isDesktop: false,
      navVisible: true, // To control navbar visibility
    };
  },
  mounted() {
    this.handleResize();
    window.addEventListener('scroll', this.handleScroll);
    window.addEventListener('resize', this.checkScreenSize);
    window.addEventListener('resize', this.handleResize); 
    this.startCounting(); // Trigger counter when the page is loaded
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
    window.removeEventListener('resize', this.handleScroll);
    window.removeEventListener('resize', this.handleResize); 
  },
  methods: {
    checkScreenSize() {
      this.isMobile = window.innerWidth < 768;
    },
    toggleSidebar() {
      this.sidebarVisible = !this.sidebarVisible;
    },
    scrollToTop() {
      window.scrollTo({
        top: 0,
        behavior: 'smooth',
      });
    },
    async submitForm() {
      try {
        const response = await this.$axios.post('http://localhost:8000/api/contact/submit/', this.formData);
        this.formSubmitted = true;
        console.log("Form Submitted: ", response.data);
      } catch (error) {
        console.error("There was an error submitting the form:", error);
      }
    },
    handleScroll() {
      this.navVisible = window.scrollY <= 100;
      const sections = ['home', 'about', 'work', 'service', 'contact'];
      let foundSection = '';
      const scrollPosition =  window.scrollY;
      
      //handle navbar visibility
      this.navVisible = scrollPosition <= 100;

      if(this.isDesktop){
        this.navVisible = window.scrollY <= 100;
      }

      //show the sidebar based on scroll only when if it's not mobile
      if(!this.isMobile){
        if(scrollPosition>100){
          if(window.innerWidth >= 768){

            this.sidebarVisible = true;
          }
        } else{
          if (window.innerWidth >= 768){

            this.sidebarVisible = false;
          }
        }
      }

      sections.forEach((section) => {
        const sectionElement = this.$refs[section];
        if (sectionElement) {
          const rect = sectionElement.getBoundingClientRect();
          if (rect.top <= window.innerHeight / 2 && rect.bottom >= window.innerHeight / 2) {
            foundSection = section;
          }
        }
      });

      if (foundSection) {
        this.currentSection = foundSection;
      }
    },
    handleResize(){
      this.isDesktop = window.innerWidth >= 768;
    },
    scrollToSection(section) {
      const sectionElement = this.$refs[section];
      if (sectionElement) {
        window.scrollTo({
          top: sectionElement.offsetTop - 80, // Adjust for navbar height
          behavior: 'smooth',
        });
      }
    },
    startCounting() {
      this.incrementCounter('experienceCount', 0, 0);
      this.incrementCounter('projectsCount', 15, 1000);
      this.incrementCounter('technologiesCount', 6, 1000);
      this.incrementCounter('commitsCount', 100, 1000);
    },
    incrementCounter(counterName, target, duration) {
      let count = 0;
      const stepTime = Math.ceil(duration / target);
      const interval = setInterval(() => {
        if (count < target) {
          count++;
          this[counterName] = count;
        } else {
          clearInterval(interval);
        }
      }, stepTime);
    },
  },
};

</script>



