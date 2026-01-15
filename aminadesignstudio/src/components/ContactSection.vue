<template>
  <section id="contact" class="section">
    <div class="container">
      <div class="inner">
        <div class="heading">
          <p class="eyebrow">Let’s work together</p>
          <h2 class="title">Contact</h2>
          <p class="subtitle">
            Tell us what you're building. We'll reply with next steps and a simple plan.
          </p>
        </div>

        <div class="grid">
          <!-- LEFT: Options -->
          <div class="card">
            <h3 class="card-title">Quick options</h3>
            <p class="card-subtitle">Choose what you want to do first.</p>

            <div class="actions">
              <a
                class="primary"
                :href="emailLink"
                @click="onEmailClick"
              >
                Email us
                <span aria-hidden="true">→</span>
              </a>

              <a
                class="secondary"
                href="#"
                @click.prevent="onBookClick"
              >
                Book intro call (coming soon)
                <span aria-hidden="true">↗</span>
              </a>
            </div>

            <div class="small">
              <p class="small-label">Email</p>
              <p class="small-value">{{ email }}</p>
              <p class="small-note">
                Prefer a call? Hit “Book intro call” and we'll send times manually until Calendly is set.
              </p>
            </div>
          </div>

          <!-- RIGHT: Form -->
          <form class="card form" @submit.prevent="submit">
            <div class="form-head">
              <h3 class="card-title">Start a project</h3>
              <p class="card-subtitle">A short intake — we'll respond within 1-2 business days.</p>
            </div>

            <div class="fields">
              <label class="field">
                <span>Name</span>
                <input v-model.trim="form.name" type="text" placeholder="Your name" required />
              </label>

              <label class="field">
                <span>Email</span>
                <input v-model.trim="form.email" type="email" placeholder="you@email.com" required />
              </label>

              <label class="field">
                <span>What do you need?</span>
                <select v-model="form.need" required>
                  <option disabled value="">Select one</option>
                  <option>Website / landing page</option>
                  <option>Product UX / flows</option>
                  <option>Design system</option>
                  <option>Shopify / e-commerce</option>
                  <option>Other</option>
                </select>
              </label>

              <label class="field">
                <span>Project details</span>
                <textarea
                  v-model.trim="form.details"
                  rows="4"
                  placeholder="What are you building, and what's the goal?"
                  required
                />
              </label>
            </div>

            <div class="form-actions">
              <button class="primary-btn" type="submit">
                Send inquiry
                <span aria-hidden="true">→</span>
              </button>

              <p class="helper" v-if="status === 'success'">
                Sent! Your email app should open — if it doesn't, copy the message and email us.
              </p>
            </div>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ContactSection",
  data() {
    return {
      email: "hello@aminadesignco.com", // change this when ready
      status: "idle",
      form: {
        name: "",
        email: "",
        need: "",
        details: "",
      },
    };
  },
  computed: {
    emailLink() {
      const subject = encodeURIComponent("Project inquiry — Amina Design Co.");
      const body = encodeURIComponent(
        `Hi Amina Design Co.,\n\nName: ${this.form.name || "[Your name]"}\nEmail: ${
          this.form.email || "[Your email]"
        }\nNeed: ${this.form.need || "[What you need]"}\n\nDetails:\n${
          this.form.details || "[Project details]"
        }\n\nThanks!`
      );
      return `mailto:${this.email}?subject=${subject}&body=${body}`;
    },
  },
  methods: {
    onBookClick() {
      // For now: just scroll + set a tiny hint
      this.status = "idle";
      // You can later replace with Calendly link:
      // window.open("https://calendly.com/YOURNAME/intro", "_blank", "noopener,noreferrer");
      alert("Calendly isn't set yet — email us and we'll send available times.");
    },
    onEmailClick() {
      // no-op (mailto handles it)
    },
    submit() {
      // simple, reliable MVP: open mail client prefilled
      this.status = "success";
      window.location.href = this.emailLink;
    },
  },
};

</script>

<style scoped>
.section {
  padding: var(--space-2xl) 0;
}

.inner {
  background: linear-gradient(180deg, rgba(255, 255, 255, 0.04), rgba(255, 255, 255, 0.02));
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 28px;
  padding: clamp(1.4rem, 5vw, 2.6rem);
  box-shadow: var(--shadow-card);
}

.heading {
  display: grid;
  gap: 0.35rem;
  margin-bottom: var(--space-lg);
}

.eyebrow {
  font-size: 0.85rem;
  letter-spacing: 0.16em;
  text-transform: uppercase;
  color: rgba(148, 163, 184, 0.85);
  margin: 0;
}

.title {
  font-size: clamp(1.9rem, 4vw, 2.6rem);
  font-weight: 900;
  margin: 0;
}

.subtitle {
  color: rgba(226, 232, 240, 0.82);
  margin: 0;
  max-width: 60ch;
}

.grid {
  display: grid;
  gap: 1rem;
}

.card {
  background: rgba(255, 255, 255, 0.03);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 18px;
  padding: 1.2rem 1.2rem;
}

.card-title {
  margin: 0;
  font-size: 1.15rem;
  font-weight: 800;
  color: #f8fafc;
}

.card-subtitle {
  margin: 0.35rem 0 0;
  color: rgba(226, 232, 240, 0.78);
  line-height: 1.6;
}

.actions {
  margin-top: 1rem;
  display: grid;
  gap: 0.75rem;
}

.primary,
.secondary {
  display: inline-flex;
  justify-content: space-between;
  align-items: center;
  gap: 0.5rem;
  text-decoration: none;
  padding: 0.9rem 1rem;
  border-radius: 14px;
  font-weight: 800;
}

.primary {
  background: linear-gradient(135deg, #a855f7, #38bdf8);
  color: #0f172a;
  box-shadow: 0 12px 24px rgba(56, 189, 248, 0.28);
}

.secondary {
  border: 1px solid rgba(255, 255, 255, 0.14);
  background: rgba(255, 255, 255, 0.04);
  color: rgba(226, 232, 240, 0.92);
}

.small {
  margin-top: 1rem;
  border-top: 1px solid rgba(255, 255, 255, 0.08);
  padding-top: 1rem;
}

.small-label {
  margin: 0;
  font-size: 0.85rem;
  color: rgba(148, 163, 184, 0.9);
}

.small-value {
  margin: 0.3rem 0 0;
  font-weight: 800;
}

.small-note {
  margin: 0.65rem 0 0;
  color: rgba(226, 232, 240, 0.75);
  line-height: 1.6;
}

.form-head {
  margin-bottom: 1rem;
}

.fields {
  display: grid;
  gap: 0.85rem;
}

.field {
  display: grid;
  gap: 0.35rem;
  color: rgba(226, 232, 240, 0.92);
  font-weight: 700;
  font-size: 0.95rem;
}

input,
select,
textarea {
  width: 100%;
  padding: 0.85rem 0.95rem;
  border-radius: 14px;
  border: 1px solid rgba(255, 255, 255, 0.12);
  background: rgba(15, 23, 42, 0.55);
  color: rgba(226, 232, 240, 0.95);
  outline: none;
}

input:focus,
select:focus,
textarea:focus {
  border-color: rgba(56, 189, 248, 0.45);
}

.form-actions {
  margin-top: 1rem;
  display: grid;
  gap: 0.75rem;
}

.primary-btn {
  border: none;
  background: linear-gradient(135deg, #a855f7, #38bdf8);
  color: #0f172a;
  font-weight: 900;
  padding: 0.95rem 1rem;
  border-radius: 14px;
  display: inline-flex;
  justify-content: space-between;
  align-items: center;
  gap: 0.5rem;
  cursor: pointer;
}

.helper {
  margin: 0;
  color: rgba(226, 232, 240, 0.78);
  line-height: 1.6;
}

@media (min-width: 900px) {
  .grid {
    grid-template-columns: 1fr 1.2fr;
    gap: 1.2rem;
    align-items: start;
  }
}
</style>
