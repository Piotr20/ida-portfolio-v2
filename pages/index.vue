<template>
  <div>
    <Header />
    <IntroSection />
    <TextBox text="portfolio" scrollID="portfolio" />
    <ProjectsSection />
    <TextBox text="Om mig" scrollID="about" />
    <AboutMe />
    <TechnicalSkills />
    <Competencies />
    <Language />
    <TextBox text="cv" scrollID="cv" />
    <WorkExpierience />
    <Education />
    <FreelanceProjects />
    <CvDownloadSection />
    <Contact />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'IndexPage',
})
</script>
