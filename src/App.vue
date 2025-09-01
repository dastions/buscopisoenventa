<template>
  <div id="app">
    <!-- Header -->
    <header class="header">
      <div class="container">
        <div class="header-content">
          <div class="logo">
            <h1>Finques el Portal 22</h1>
            <span>Inmobiliaria catalunya</span>
          </div>
          <nav class="nav">
            <a href="mailto:finqueselportal@gmail.com" class="contact-btn">
              📧 Contactar
            </a>
          </nav>
        </div>
      </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        
      <div class="container">
        <div class="hero-content">
          <div class="hero-text">
            <h2>Tu hogar ideal en España y Catalunya te está esperando</h2>
            <p>Portal 22 es tu inmobiliaria de confianza para comprar pisos en España y Catalunya. Encuentra las mejores propiedades urbanas en Barcelona, Madrid, Valencia y otras ciudades españolas, así como fincas rústicas en entornos naturales únicos. Asesoramiento profesional en compraventa de inmuebles.</p>
            <div class="hero-buttons">
              <button @click="goToPisos" class="btn btn-primary">
                🏢 Ver Pisos
              </button>
              <button @click="goToFincas" class="btn btn-secondary">
                🌾 Fincas Rústicas
              </button>
            </div>
          </div>
          <div class="hero-image">
            <div class="property-showcase">
              <div class="property-card">
                <div class="property-placeholder">🏠</div>
                <h3>Pisos modernos</h3>
              </div>
              <div class="property-card">
                <div class="property-placeholder">🏞️</div>
                <h3>Fincas rústicas</h3>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact Form Section -->
    <section class="contact-form-section">
      <div class="container">
        <div class="form-wrapper">
          <h3>¿Buscas comprar un piso en España o Catalunya?</h3>
          <p>Completa el formulario y nuestros expertos inmobiliarios te asesorarán personalmente sobre las mejores opciones para tu inversión</p>
          <form @submit="handleSubmit" class="contact-form">
            <div class="form-group">
              <input type="text" v-model="form.name" placeholder="Nombre completo" required>
            </div>
            <div class="form-group">
              <input type="email" v-model="form.email" placeholder="Email" required>
            </div>
            <div class="form-group">
              <input type="tel" v-model="form.phone" placeholder="Teléfono">
            </div>
            <div class="form-group">
              <select v-model="form.propertyType">
                <option value="">Tipo de propiedad</option>
                <option value="piso">Piso en ciudad</option>
                <option value="apartamento">Apartamento</option>
                <option value="casa">Casa unifamiliar</option>
                <option value="finca">Finca rústica</option>
                <option value="local">Local comercial</option>
                <option value="otro">Otro</option>
              </select>
            </div>
            <div class="form-group">
              <textarea v-model="form.message" placeholder="Mensaje" rows="4" required></textarea>
            </div>
            <button type="submit" class="btn btn-primary btn-full">
              Enviar consulta
            </button>
          </form>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
      <div class="container">
        <div class="footer-content">
          <div class="footer-section">
            <h4>Portal 22</h4>
            <p>Tu inmobiliaria de confianza en España y Catalunya</p>
            <p>Especialistas en compraventa de pisos y propiedades</p>
          </div>
          <div class="footer-section">
            <h4>Contacto</h4>
            <div class="contact-info">
              <p>📧 finqueselportal@gmail.com</p>
              <p>📞 +34  606 83 27 53</p>
              <p>📍 43330, Riudoms, Tarragona</p>
            </div>
          </div>
          <div class="footer-section">
            <h4>Servicios</h4>
            <ul>
              <li><a href="https://www.buscofincarustica.com/" @click="goToPisos">Pisos en España</a></li>
              <li><a href="https://www.buscofincarustica.com/" @click="goToFincas">Fincas Rústicas</a></li>
              <li><a href="mailto:finqueselportal@gmail.com">Valoraciones</a></li>
              <li><a href="mailto:finqueselportal@gmail.com">Asesoramiento legal</a></li>
              <li><a href="mailto:finqueselportal@gmail.com">Financiación</a></li>
            </ul>
          </div>
          <div class="footer-section">
            <h4>Datos Fiscales</h4>
            <p>Portal 22 S.L.</p>
          </div>
        </div>
        <div class="footer-bottom">
          <p>&copy; 2025 Portal 22. Todos los derechos reservados.</p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      form: {
        name: '',
        email: '',
        phone: '',
        propertyType: '',
        message: ''
      }
    }
  },
  methods: {
    goToPisos() {
      // Simular navegación a página de pisos
      const basePath = process.env.NODE_ENV === 'production' ? '/' : './'
      window.location.href = basePath + 'pisos.html'
    },
    goToFincas() {
      // Simular navegación a página de fincas
      const basePath = process.env.NODE_ENV === 'production' ? '/' : './'
      window.location.href = basePath + 'fincas.html'
    },
    handleSubmit(e) {
      e.preventDefault()
      
      // Crear el contenido del email
      const subject = `Consulta desde web - ${this.form.propertyType || 'General'}`
      const body = `
Nombre: ${this.form.name}
Email: ${this.form.email}
Teléfono: ${this.form.phone || 'No proporcionado'}
Tipo de propiedad: ${this.form.propertyType || 'No especificado'}

Mensaje:
${this.form.message}
      `.trim()
      
      // Crear el enlace mailto
      const mailtoLink = `mailto:finqueselportal@gmail.com?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`
      
      // Abrir el cliente de email
      window.location.href = mailtoLink
    }
  }
}
</script>
