const units = {
  length: {
    m: ['Meters (m)', 1],
    km: ['Kilometers (km)', 1000],
    cm: ['Centimeters (cm)', 0.01],
    mm: ['Millimeters (mm)', 0.001],
    inch: ['Inches (in)', 0.0254],
    ft: ['Feet (ft)', 0.3048],
    mi: ['Miles (mi)', 1609.344],
  },
  mass: {
    kg: ['Kilograms (kg)', 1],
    g: ['Grams (g)', 0.001],
    lb: ['Pounds (lb)', 0.45359237],
    oz: ['Ounces (oz)', 0.028349523125],
  },
  temp: {
    c: ['Celsius (°C)'],
    f: ['Fahrenheit (°F)'],
    k: ['Kelvin (K)'],
  },
};

function convert(value, type, from, to) {
  if (type !== 'temp') {
    return value * units[type][from][1] / units[type][to][1];
  }

  const celsius = from === 'c'
    ? value
    : from === 'f'
      ? (value - 32) * 5 / 9
      : value - 273.15;

  if (to === 'c') {
    return celsius;
  }

  return to === 'f'
    ? celsius * 9 / 5 + 32
    : celsius + 273.15;
}

if (typeof module !== 'undefined') {
  module.exports = { convert, units };
}
