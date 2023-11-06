function startStory() {
    console.log("Welkom bij het interactieve verhaal!");
    console.log("Je staat voor een kruispunt.");
  
    makeChoice("Links gaan", leftPath);
    makeChoice("Rechts gaan", rightPath);
  }
  
  function leftPath() {
    console.log("Je gaat naar links en komt een brug tegen.");
  
    makeChoice("Over de brug gaan", crossBridge);
    makeChoice("Onder de brug door gaan", underBridge);
  }
  
  function rightPath() {
    console.log("Je gaat naar rechts en ziet een donker bos.");
  
    makeChoice("Het bos in gaan", enterForest);
    makeChoice("Een andere route kiezen", startStory);
  }
  
  function crossBridge() {
    console.log("Je steekt de brug over en komt een vriendelijke dwerg tegen.");
    console.log("De dwerg geeft je een kaart en wijst je de weg.");
  
    // Het verhaal kan hier verder gaan met nieuwe keuzes
  }
  
  function underBridge() {
    console.log("Je gaat onder de brug door en vindt een verborgen tunnel.");
  
    makeChoice("De tunnel verkennen", exploreTunnel);
    makeChoice("Terugkeren naar het kruispunt", startStory);
  }
  
  function enterForest() {
    console.log("Je betreedt het bos en hoort mysterieuze geluiden.");
  
    makeChoice("Verder het bos in gaan", deeperIntoForest);
    makeChoice("Terugkeren naar het kruispunt", startStory);
  }
  
  function exploreTunnel() {
    console.log("Je verkent de tunnel en ontdekt een geheime schat!");
  
    // Het verhaal kan hier verder gaan met nieuwe keuzes
  }
  
  function deeperIntoForest() {
    console.log("Je gaat dieper het bos in en ontmoet een wijze tovenaar.");
  
    // Het verhaal kan hier verder gaan met nieuwe keuzes
  }
  
  function makeChoice(prompt, nextFunction) {
    console.log(`- ${prompt}`);
    const choice = prompt("Maak je keuze (voer het nummer in): ");
    nextFunction();
  }
  
  // Start het verhaal
  startStory();
