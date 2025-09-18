require([
  "esri/WebScene",
  "esri/views/SceneView",
  "esri/widgets/Legend",
  "esri/widgets/LayerList",
  "esri/widgets/Search"
], function(WebScene, SceneView, Legend, LayerList, Search) {

  // Web Scene IDs
  const chicagoSceneId = "fef6868cafcc420eb4bc2e78d54c38d7"; // Replace with actual Chicago webscene ID
  const bostonSceneId = "8046207c1c214b5587230f5e5f8efc77"; // Replace with actual Boston webscene ID

  // Create WebScenes
  const chicagoScene = new WebScene({ portalItem: { id: chicagoSceneId } });
  const bostonScene = new WebScene({ portalItem: { id: bostonSceneId } });

  // Initialize SceneView with Chicago as default
  const view = new SceneView({
    container: "viewDiv",
    map: chicagoScene,
    camera: {
      position: { x: -87.6298, y: 41.8781, z: 500 },
      tilt: 65,
      heading: 0
    }
  });

  // Add widgets
  const legend = new Legend({ view });
  const layerList = new LayerList({ view });
  const searchWidget = new Search({ view });

  view.ui.add(legend, "bottom-left");
  view.ui.add(layerList, "top-left");
  view.ui.add(searchWidget, "top-left");

  // --- Switch Button Logic ---
  const switchBtn = document.getElementById("switchBtn");
  let showingChicago = true;

  switchBtn.addEventListener("click", () => {
    if(showingChicago) {
      // Switch to Boston
      view.map = bostonScene;
      view.camera.position = { x: -71.0589, y: 42.3601, z: 500 };
      view.camera.tilt = 65;
      view.camera.heading = 0;
      switchBtn.textContent = "Chicago";
    } else {
      // Switch to Chicago
      view.map = chicagoScene;
      view.camera.position = { x: -87.6298, y: 41.8781, z: 500 };
      view.camera.tilt = 65;
      view.camera.heading = 0;
      switchBtn.textContent = "Boston";
    }
    showingChicago = !showingChicago;
  });

});
