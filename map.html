// Initialize the map
const map = L.map('map');
const bounds = [];

// Load OpenStreetMap tiles
L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    attribution: '© OpenStreetMap contributors'
}).addTo(map);

// Define custom marker icons
const greenIcon = new L.Icon({
    iconUrl: 'https://raw.githubusercontent.com/pointhi/leaflet-color-markers/master/img/marker-icon-2x-green.png',
    shadowUrl: 'https://unpkg.com/leaflet@1.9.3/dist/images/marker-shadow.png',
    iconSize: [25, 41],
    iconAnchor: [12, 41],
    popupAnchor: [1, -34],
    shadowSize: [41, 41]
});

const grayIcon = new L.Icon({
    iconUrl: 'https://raw.githubusercontent.com/pointhi/leaflet-color-markers/master/img/marker-icon-2x-grey.png',
    shadowUrl: 'https://unpkg.com/leaflet@1.9.3/dist/images/marker-shadow.png',
    iconSize: [25, 41],
    iconAnchor: [12, 41],
    popupAnchor: [1, -34],
    shadowSize: [41, 41]
});

// Fetch the same sites.json file used by the database page
fetch('sites.json')
    .then(response => response.json())
    .then(sites => {
        sites.forEach(site => {
            const isVerified = site.processVerified === true;

            const marker = L.marker([site.lat, site.lng], {
                icon: isVerified ? greenIcon : grayIcon
            }).addTo(map);

            marker.bindPopup(`
                <b>${site.location}</b><br>
                ${site.address}<br>
                <strong>Facility Type:</strong> ${site.facilityType}<br>
                <strong>Status:</strong> ${isVerified ? "Verified" : "Process Not Verified"}<br>
                <a href="${site.website}" target="_blank" rel="noopener noreferrer">Website</a><br>
                <em>Last checked: ${site.dateLastChecked}</em>
            `);

            bounds.push([site.lat, site.lng]);
        });

        // Fit map to markers
        if (bounds.length > 0) {
            map.fitBounds(bounds, { padding: [50, 50] });
        }
    })
    .catch(err => console.error("Error loading site data:", err));

// Add map legend
const legend = L.control({ position: "bottomright" });
legend.onAdd = function () {
    const div = L.DomUtil.create("div", "legend");
    div.innerHTML = `
        <h4>Legend</h4>
        <p><img src="https://raw.githubusercontent.com/pointhi/leaflet-color-markers/master/img/marker-icon-2x-green.png" alt="Green icon"> Verified</p>
        <p><img src="https://raw.githubusercontent.com/pointhi/leaflet-color-markers/master/img/marker-icon-2x-grey.png" alt="Gray icon"> Process Not Verified</p>
    `;
    return div;
};
legend.addTo(map);
