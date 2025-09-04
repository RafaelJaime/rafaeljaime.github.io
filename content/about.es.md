+++
date = '2025-09-03T12:42:03+02:00'
draft = false
title = 'Acerca de'
translationKey = 'about'
+++

{{< rawhtml >}}
<style>
  .hero-section {
    background: var(--theme);
    padding: 4rem 0;
    text-align: center;
    color: var(--primary);
    margin-bottom: 3rem;
    position: relative;
    overflow: hidden;
    border-radius: 20px;
    border: 1px solid var(--border);
  }

  .hero-section::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 100" fill="rgba(102,126,234,0.1)"><polygon points="0,0 1000,100 1000,0"/></svg>') no-repeat center bottom;
    background-size: 100% 100px;
  }

  .hero-content {
    position: relative;
    z-index: 1;
  }

  .hero-title {
    font-size: 3.5rem;
    font-weight: 700;
    margin-bottom: 1rem;
    animation: fadeInUp 1s ease-out;
    color: var(--primary);
  }

  .hero-subtitle {
    font-size: 1.3rem;
    opacity: 0.8;
    animation: fadeInUp 1s ease-out 0.2s both;
    color: var(--secondary);
  }

  .section {
    margin-bottom: 4rem;
    padding: 2rem;
    background: var(--entry);
    border-radius: 15px;
    border: 1px solid var(--border);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  .section:hover {
    transform: translateY(-5px);
    box-shadow: 0 20px 40px rgba(102,126,234,0.15);
  }

  .section-title {
    font-size: 2.5rem;
    color: var(--primary);
    margin-bottom: 2rem;
    position: relative;
    display: inline-block;
  }

  .section-title::after {
    content: '';
    position: absolute;
    bottom: -5px;
    left: 0;
    width: 50px;
    height: 3px;
    background: linear-gradient(90deg, #667eea, #764ba2);
    border-radius: 2px;
  }

  .experience-item {
    background: var(--code-bg);
    padding: 2rem;
    border-radius: 10px;
    margin-bottom: 2rem;
    border-left: 4px solid #667eea;
    transition: all 0.3s ease;
    border: 1px solid var(--border);
  }

  .experience-item:hover {
    transform: translateX(5px);
    box-shadow: 0 10px 20px rgba(102,126,234,0.2);
  }

  .company-name {
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--primary);
    margin-bottom: 0.5rem;
  }

  .job-title {
    color: #667eea;
    font-weight: 600;
    margin-bottom: 0.5rem;
  }

  .job-duration {
    color: var(--secondary);
    font-style: italic;
    margin-bottom: 1rem;
  }

  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
    margin: 2rem 0;
  }

  .skill-category {
    background: var(--code-bg);
    padding: 2rem;
    border-radius: 15px;
    text-align: center;
    border: 1px solid var(--border);
    transition: all 0.3s ease;
  }

  .skill-category:hover {
    box-shadow: 0 10px 20px rgba(102,126,234,0.1);
  }

  .skill-category h4 {
    color: var(--primary);
    font-size: 1.3rem;
    margin-bottom: 1.5rem;
    font-weight: 600;
  }

  .tech-icons {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 1.5rem;
    margin: 1.5rem 0;
  }

  .tech-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 1rem;
    background: var(--entry);
    border-radius: 10px;
    border: 1px solid var(--border);
    transition: all 0.3s ease;
    min-width: 80px;
  }

  .tech-item:hover {
    transform: translateY(-5px) scale(1.05);
    box-shadow: 0 15px 25px rgba(102,126,234,0.3);
  }

  .tech-item img {
    width: 40px;
    height: 40px;
    margin-bottom: 0.5rem;
  }

  .tech-item p {
    font-size: 0.8rem;
    font-weight: 600;
    color: var(--primary);
    margin: 0;
  }

  .education-item {
    background: var(--code-bg);
    padding: 2rem;
    border-radius: 15px;
    margin-bottom: 1.5rem;
    position: relative;
    overflow: hidden;
    border: 1px solid var(--border);
    transition: all 0.3s ease;
  }

  .education-item:hover {
    box-shadow: 0 10px 20px rgba(102,126,234,0.1);
  }

  .education-item::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 5px;
    height: 100%;
    background: linear-gradient(135deg, #ff7b54 0%, #ff6b35 100%);
  }

  .school-name {
    font-size: 1.3rem;
    font-weight: 700;
    color: #ff6b35;
    margin-bottom: 0.5rem;
  }

  .degree {
    color: var(--primary);
    font-weight: 600;
    margin-bottom: 0.5rem;
  }

  .education-duration {
    color: var(--secondary);
    font-style: italic;
    margin-bottom: 1rem;
  }

  .contact-section {
    background: var(--code-bg);
    color: var(--primary);
    text-align: center;
    padding: 3rem 2rem;
    border-radius: 20px;
    margin-top: 3rem;
    border: 2px solid #667eea;
    position: relative;
    overflow: hidden;
  }

  .contact-section::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(135deg, rgba(102,126,234,0.1) 0%, rgba(118,75,162,0.1) 100%);
    z-index: 0;
  }

  .contact-section > * {
    position: relative;
    z-index: 1;
  }

  .contact-links {
    display: flex;
    justify-content: center;
    gap: 2rem;
    margin-top: 2rem;
    flex-wrap: wrap;
  }

  .contact-link {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    padding: 0.8rem 1.5rem;
    background: #667eea;
    color: white;
    text-decoration: none;
    border-radius: 25px;
    font-weight: 600;
    transition: all 0.3s ease;
  }

  .contact-link:hover {
    background: #5a67d8;
    transform: translateY(-2px);
    text-decoration: none;
    color: white;
    box-shadow: 0 10px 20px rgba(102,126,234,0.4);
  }

  [data-theme="dark"] .hero-section::before {
    background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 100" fill="rgba(102,126,234,0.2)"><polygon points="0,0 1000,100 1000,0"/></svg>') no-repeat center bottom;
  }

  [data-theme="dark"] .tech-item img {
    filter: brightness(0.9);
  }

  @keyframes fadeInUp {
    from {
      opacity: 0;
      transform: translateY(30px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  .animate-on-scroll {
    opacity: 0;
    transform: translateY(30px);
    transition: all 0.6s ease;
  }

  .animate-on-scroll.visible {
    opacity: 1;
    transform: translateY(0);
  }

  @media (max-width: 768px) {
    .hero-title {
      font-size: 2.5rem;
    }
    
    .skills-grid {
      grid-template-columns: 1fr;
    }
    
    .tech-icons {
      gap: 1rem;
    }
    
    .contact-links {
      flex-direction: column;
      align-items: center;
    }
  }
</style>

<div class="hero-section">
  <div class="hero-content">
    <h1 class="hero-title">Rafael Jaime</h1>
    <p class="hero-subtitle">Desarrollador apasionado por la tecnología e innovación</p>
  </div>
</div>

<div class="container">
  <div class="section animate-on-scroll">
    <h2 class="section-title">💼 Experiencia Profesional</h2>
    
    <div class="experience-item">
      <div class="company-name">ALTEN Spain</div>
      <div class="job-title">iOS Developer | Full-time | Remoto</div>
      <div class="job-duration">Febrero 2022 - Enero 2024 (2 años)</div>
      <ul>
        <li>Desarrollo de aplicaciones iOS con Swift y SwiftUI</li>
        <li>Implementación de arquitectura MVVM y mejores prácticas de desarrollo iOS</li>
      </ul>
    </div>

    <div class="experience-item">
      <div class="company-name">ALTEN Spain</div>
      <div class="job-title">Junior iOS Developer | Contrato</div>
      <div class="job-duration">Junio 2021 - Febrero 2022 (9 meses)</div>
      <ul>
        <li>Desarrollo iOS usando Swift</li>
        <li>Experiencia con CocoaPods y arquitectura MVC</li>
      </ul>
    </div>

    <div class="experience-item">
      <div class="company-name">ALTEN Spain</div>
      <div class="job-title">iOS Development Intern – Swift & Objective-C | Prácticas</div>
      <div class="job-duration">Marzo 2021 - Junio 2021 (4 meses)</div>
      <ul>
        <li>Desarrollo de aplicaciones para iOS usando Swift y Objective-C</li>
        <li>Implementación de UI e integración de funcionalidades nativas</li>
        <li>Trabajo con CocoaPods y patrón arquitectónico MVC</li>
      </ul>
    </div>
  </div>

  <div class="section animate-on-scroll">
    <h2 class="section-title">🚀 Habilidades Técnicas</h2>
    
    <div class="skills-grid">
      <div class="skill-category">
        <h4>Lenguajes de Programación</h4>
        <div class="tech-icons">
          <div class="tech-item">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/swift/swift-original.svg" alt="Swift">
            <p>Swift</p>
          </div>
          <div class="tech-item">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" alt="Java">
            <p>Java</p>
          </div>
          <div class="tech-item">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="Python">
            <p>Python</p>
          </div>
          <div class="tech-item">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="JavaScript">
            <p>JavaScript</p>
          </div>
        </div>
      </div>

      <div class="skill-category">
        <h4>Frameworks & Librerías</h4>
        <div class="tech-icons">
          <div class="tech-item">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/apple/apple-original.svg" alt="SwiftUI">
            <p>SwiftUI</p>
          </div>
          <div class="tech-item">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/pandas/pandas-original.svg" alt="Pandas">
            <p>Pandas</p>
          </div>
          <div class="tech-item">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg" alt="React">
            <p>React</p>
          </div>
          <div class="tech-item">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/spring/spring-original.svg" alt="Spring Boot">
            <p>Spring Boot</p>
          </div>
        </div>
      </div>

      <div class="skill-category">
        <h4>Herramientas & Tecnologías</h4>
        <div class="tech-icons">
          <div class="tech-item">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/git/git-original.svg" alt="Git">
            <p>Git</p>
          </div>
          <div class="tech-item">
            <img src="https://upload.wikimedia.org/wikipedia/commons/9/93/Amazon_Web_Services_Logo.svg" alt="AWS">
            <p>AWS</p>
          </div>
          <div class="tech-item">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original.svg" alt="PostgreSQL">
            <p>PostgreSQL</p>
          </div>
          <div class="tech-item">
            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/apache/apache-original.svg" alt="Apache Spark">
            <p>Apache Spark</p>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="section animate-on-scroll">
    <h2 class="section-title">🎓 Educación</h2>
    
    <div class="education-item">
      <div class="school-name">IES Rafael Alberti</div>
      <div class="degree">Técnico Superior en Inteligencia Artificial y Big Data</div>
      <div class="education-duration">Octubre 2024 - Junio 2025</div>
      <p><strong>Habilidades:</strong> Machine Learning, Apache Spark, Programming, Big Data, Data Science, PostgreSQL, Matplotlib, Pandas, AWS, ETL</p>
    </div>

    <div class="education-item">
      <div class="school-name">CDP San Ignacio: Salesianos-Cádiz</div>
      <div class="degree">Técnico Superior en Desarrollo de Aplicaciones Multiplataforma</div>
      <div class="education-duration">Septiembre 2019 - Junio 2021</div>
      <p><strong>Habilidades:</strong> Java, Programming, Object-Oriented Programming (OOP)</p>
    </div>

    <div class="education-item">
      <div class="school-name">IES Mar de Cádiz</div>
      <div class="degree">Técnico en Sistemas Microinformáticos y Redes</div>
      <div class="education-duration">Septiembre 2017 - Junio 2019</div>
      <p><strong>Habilidades:</strong> Linux</p>
    </div>
  </div>
</div>

<div class="contact-section animate-on-scroll">
  <h2 style="margin-bottom: 1rem;">📫 ¡Conectemos!</h2>
  <p>¿Tienes un proyecto interesante? ¡Me encantaría conocer más!</p>
  
  <div class="contact-links">
    <a href="https://github.com/RafaelJaime" class="contact-link" target="_blank">
      🐙 GitHub
    </a>
    <a href="https://huggingface.co/RafaelJaime" class="contact-link" target="_blank">
      🤗 HuggingFace
    </a>
    <a href="https://www.linkedin.com/in/rafael-jaime-moreno-665112227/" class="contact-link" target="_blank">
      💼 LinkedIn
    </a>
    <a href="mailto:rajaimor@gmail.com" class="contact-link">
      📧 Email
    </a>
  </div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible');
      }
    });
  }, {
    threshold: 0.1
  });

  document.querySelectorAll('.animate-on-scroll').forEach(el => {
    observer.observe(el);
  });
});
</script>
{{< /rawhtml >}}