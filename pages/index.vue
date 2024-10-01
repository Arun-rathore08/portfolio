<template>
  <div class="min-h-screen bg-black text-white font-sans">
    <div class="container mx-auto py-10 px-5 md:px-20">
      <!-- Logo -->
      
      <!-- Navigation -->
      <div :class="['fixed top-0 left-0 h-full w-54 bg-black transition-transform duration-300', sidebarVisible ? 'translate-x-0' : '-translate-x-full']">
        
          <nuxt-link to="/"><img src="/logo.png" style="width: 75px; margin: 2px;" alt=""></nuxt-link>
        
        <nav class="flex flex-col items-center space-y-6 mt-10 text-white" style="font-size: large;">
          <NuxtLink to="/" class="hover:text-blue-400">Home</NuxtLink>
          <NuxtLink to="/#about" class="hover:text-blue-400">About</NuxtLink>
          <NuxtLink to="/#work" class="hover:text-blue-400">Work</NuxtLink>
          <NuxtLink to="/#service" class="hover:text-blue-400">Services</NuxtLink>
          <NuxtLink to="/#contact" class="hover:text-blue-400">Contact</NuxtLink>
        </nav>
    </div>

    <!-- Normal Navbar -->
    <nav class="fixed top-0 left-0 w-full bg-black text-white py-5 px-10 z-20 transition-all duration-300" :class="{'hidden': sidebarVisible}">
      <div style="display: flex; justify-content: space-around;">
        <nuxt-link to="/"><img src="/logo.png" style="width: 75px;" alt=""></nuxt-link>
        <ul class="flex justify-end space-x-8 pt-2" style="font-size: large;">
          <li><NuxtLink to="/" class="hover:text-blue-400">Home</NuxtLink></li>
          <li><NuxtLink to="/#about" class="hover:text-blue-400">About</NuxtLink></li>
          <li><NuxtLink to="/#work" class="hover:text-blue-400">Work</NuxtLink></li>
          <li><NuxtLink to="/#service" class="hover:text-blue-400">Services</NuxtLink></li>
          <li><NuxtLink to="/#contact" class="hover:text-blue-400">Contact</NuxtLink></li>
        </ul>
      </div>
    </nav>
      <div class="cont" style="margin-left: 30px;">

        <!-- Hero Section -->
        <section class="flex flex-col md:flex-row items-center justify-between py-20">
          <!-- Text Section -->
          <div class="md:w-1/2">
          <h2 class="text-gray-500 text-xl">Software Developer</h2>
          <h1 class="text-6xl font-extrabold">
            Hello I'm <br />
            <span class="text-green-400">Arun Rathore</span>
          </h1>
          <p class="text-gray-400 mt-4">
            I excel at crafting elegant digital experiences and am proficient in various programming languages and technologies.
          </p>
          <div class="mt-8 flex items-center space-x-4">
            <button class="bg-#00bfa6-400 text-black px-6 py-3 rounded-full" download-btn>Download CV</button>
          </div>
        </div>
        
        <!-- Image Section -->
        <!-- Image Section -->
        <div class="relative flex justify-center items-center md:w-2/5">
          <!-- Main Image -->
          <div class="image-container">
            <!-- Main Image -->
            <img
            src="/ar.jpg"
            alt="Profile"
            class="w-65 h-65 rounded object-cover z-10"
            />
            <!-- Circular Moving Lines -->
            
            <div class="circular-anim"></div>
          </div>
        </div>
        
      </section>
      <div class="container mx-auto py-32 px-5">
      
      <!-- Experience Section -->
      <section class="text-center py-5">
        <div class="flex flex-wrap justify-center space-x-4 sm:space-x-6 md:spacs-x-10 text-2xl">
          <div>
            <p class="font-bold text-white">0</p>
            <p class="text-gray-500">Years of experience</p>
          </div>
          <div>
            <p class="font-bold text-white">15</p>
            <p class="text-gray-500">Projects completed</p>
          </div>
          <div>
            <p class="font-bold text-white">6</p>
            <p class="text-gray-500">Technologies mastered</p>
          </div>
          <div>
            <p class="font-bold text-white">100</p>
            <p class="text-gray-500">Code commits</p>
          </div>
        </div>
      </section>
    </div><hr />
      <!-- Add your content here -->
       <section id="about">
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
              <li class="lt">M.Tech in Computer Science (2023 - Present) - XYZ University</li>
              <li class="lt">B.Tech in Computer Science (2019 - 2023) - ABC College</li>
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
          <section id="work">
             <section class="portfolio-gallery">
               <h3 style="text-align: center; font-weight: bold; font-size: large;">My Work</h3>
               <div class="gallery">
                 <!-- Project 1: AI ChatBot -->
                 <div class="gallery-item">
                   <img src="/ai.png" alt="AI ChatBot" />
                   <h4>AI ChatBot</h4>
                   <p>This AI chatbot is built using Python, Django, and JavaScript. It automates responses based on user queries, making interaction seamless.</p>
                   <ul>
                     <li>Technologies: Python, Django, SQLite, HTML, CSS, JavaScript</li>
                     <li>Created by: Arun Rathore</li>
                   </ul>
                   <a href="https://github.com/Arun-rathore08/ChatBot" target="_blank">View on GitHub</a>
                 </div>
    
                 <!-- Project 2: ToDo List App -->
                 <div class="gallery-item">
                   <img src="/todo.png" alt="ToDo List App" />
                   <h4>ToDo List App</h4>
                   <p>A simple and effective ToDo app to manage tasks, built with Python, Django, and Bootstrap for an intuitive UI and smooth functionality.</p>
                   <ul>
                     <li>Technologies: Python, Django, SQLite, HTML, CSS, Bootstrap</li>
                     <li>Created by: Arun Rathore</li>
                   </ul>
                   <a href="https://github.com/Arun-rathore08/TODO-Application" target="_blank">View on GitHub</a>
                 </div>
                 
                 <!-- Project 3: Hotel Management System -->
                 <div class="gallery-item">
                   <img src="/hotel.png" alt="Hotel Management System" />
                   <h4>Hotel Management System</h4>
                   <p>A web-based solution for managing hotel operations, from bookings to customer handling. Built with PHP and MySQL.</p>
                   <ul>
                     <li>Technologies: HTML, CSS, JavaScript, PHP, MySQL</li>
                     <li>Team: Arun Rathore, Roshan Nagose, Lakhan Singh</li>
                     <li>My Role: Database creation and management</li>
                   </ul>
                   <a href="https://github.com/Arun-rathore08" target="_blank">View on GitHub</a>
                 </div>
               </div>
             </section>
          </section>
          <br /><hr />
          <section id="service">
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
       <section id="contact">
         <div class="contact-container">
           <h1>Contact Me</h1>
           <form @submit.prevent="submitForm" class="contact-form">
             <div class="form-group">
              <label for="name">Name:</label>
              <input type="text" v-model="formData.name" required placeholder="Your Name" />
            </div>
            <div class="form-group">
              <label for="email">Email:</label>
              <input type="email" v-model="formData.email" required placeholder="Your Email" />
            </div>
            <div class="form-group">
              <label for="contact">Contact Number:</label>
              <input type="text" v-model="formData.contact" required placeholder="Your Contact Number" />
            </div>
            <div class="form-group">
              <label for="message">Reason for Contact:</label>
              <textarea v-model="formData.message" required placeholder="Why do you want to connect?"></textarea>
            </div>
            <button type="submit">Submit</button>
            <p class="para" v-if="formSubmitted">Thank you! We will get back to you shortly.</p>
          </form>
        </div>

        <!-- Social links -->
        <div class="social-links">
          <a href="https://www.linkedin.com/in/arun-rathore-1b9228223" target="_blank">
            <img src="/linkedin.png" alt="LinkedIn" />
          </a>
          <a href="https://github.com/arun-rathore08" target="_blank">
            <img src="/github.png" alt="GitHub" />
          </a>
          <a href="mailto:15arunrathore@gmail.com">
            <img src="/gmail.png" alt="Email" />
          </a>
        </div>
      </section>
    </div>
  </div>
    <footer>
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
    };
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    async submitForm() {
      try {
        const response = await this.$axios.post('http://localhost:8000/api/contact/submit/', this.formData);
        this.formSubmitted = true;
        console.log("Form Submitted: ", response.data)
      } catch(error){
        console.error("There was an error submitting the form:", error);
      }
      
    },
    handleScroll() {
      const scrollPosition = window.scrollY;
      if (scrollPosition > 100) {
        this.sidebarVisible = true;
      } else {
        this.sidebarVisible = false;
      }
    },
  },
  startCounting() {
      const targetExperience = 0;
      const targetProjects = 15;
      const targetTechnologies = 6;
      const targetCommits = 100;

      this.incrementCounter('experienceCount', targetExperience, 100);
      this.incrementCounter('projectsCount', targetProjects, 100);
      this.incrementCounter('technologiesCount', targetTechnologies, 100);
      this.incrementCounter('commitsCount', targetCommits, 100);
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
  
};
</script>


