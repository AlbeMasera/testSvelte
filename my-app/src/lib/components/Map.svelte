<script lang="ts">
  import Plot from 'svelte-plotly.js';
  
    const location = [ "Belarus", "Moldova", "Lithuania", "Russia", "Romania", "Ukraine", "Andorra", "Hungary", "Czech Republic", "Slovakia", "Portugal", "Serbia", "Grenada", "Poland", "Latvia", "Finland", "South Korea", "France", "Australia", "Croatia", "Ireland", "Luxembourg", "Germany", "Slovenia", "United Kingdom", "Denmark", "Bulgaria", "Spain", "Belgium", "South Africa", "New Zealand", "Gabon", "Namibia", "Switzerland", "Saint Lucia", "Austria", "Estonia", "Greece", "Kazakhstan", "Canada", "Nigeria", "Netherlands", "Uganda", "Rwanda", "Chile", "Argentina", "Burundi", "United States", "Cyprus", "Sweden", "Venezuela", "Paraguay", "Brazil", "Sierra Leone", "Montenegro", "Belize", "Cameroon", "Botswana", "Saint Kitts and Nevis", "Guyana", "Peru", "Panama", "Niue", "Palau", "Norway", "Tanzania", "Georgia", "Uruguay", "Angola", "Laos", "Japan", "Mexico", "Ecuador", "Dominica", "Iceland", "Thailand", "Bosnia and Herzegovina", "Sao Tome and Principe", "Malta", "Albania", "Bahamas", "Dominican Republic", "Mongolia", "Cape Verde", "Barbados", "Burkina Faso", "Italy", "Trinidad and Tobago", "China", "Macedonia", "Saint Vincent and the Grenadines", "Equatorial Guinea", "Suriname", "Vietnam", "Lesotho", "Haiti", "Cook Islands", "Colombia", "Ivory Coast", "Bolivia", "Swaziland", "Zimbabwe", "Seychelles", "Cambodia", "Puerto Rico", "Netherlands Antilles", "Philippines", "Costa Rica", "Armenia", "Cuba", "Nicaragua", "Jamaica", "Ghana", "Liberia", "Uzbekistan", "Chad", "United Arab Emirates", "Kyrgyzstan", "India", "Turkmenistan", "Kenya", "Ethiopia", "Honduras", "Guinea-Bissau", "Zambia", "Republic of the Congo", "Guatemala", "Central African Republic", "North Korea", "Sri Lanka", "Mauritius", "Samoa", "Democratic Republic of the Congo", "Nauru", "Gambia", "Federated States of Micronesia", "El Salvador", "Fiji", "Papua New Guinea", "Kiribati", "Tajikistan", "Israel", "Sudan", "Malawi", "Lebanon", "Azerbaijan", "Mozambique", "Togo", "Nepal", "Brunei", "Benin", "Singapore", "Turkey", "Madagascar", "Solomon Islands", "Tonga", "Tunisia", "Tuvalu", "Qatar", "Vanuatu", "Djibouti", "Malaysia", "Syria", "Maldives", "Mali", "Eritrea", "Algeria", "Iran", "Oman", "Brunei", "Morocco", "Jordan", "Bhutan", "Guinea", "Burma", "Afghanistan", "Senegal", "Indonesia", "Timor-Leste", "Iraq", "Somalia", "Egypt", "Niger", "Yemen", "Comoros", "Saudi Arabia", "Bangladesh", "Kuwait", "Libya", "Mauritania", "Pakistan"]
    var randoms = [...Array(location.length-1)].map(() => Math.floor(Math.random()*100 ));

    var data:Plotly.Data[] = [{
        type: 'choropleth',
        locationmode: 'country names',
        locations: location,
        z: randoms,
        text: location,
        showscale: false
    }];

    var layout = {
      autosize: true,
     
      
      geo: {
          projection: {
              type: 'natural earth',
              scale: 5,
              minScale: 1,  
              
          },
         
          center: { lat: 46, lon: 8 }
      },

      };
</script>

<Plot
  data={data}
  layout={layout}
/>