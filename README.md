# formtojson

const formtojson = (e) => {
    e.preventDefault();
    let formData = new FormData(e.target);
    let object = {};
    formData.forEach((value, key) => (object[key] = value));
    let json = JSON.stringify(object);
    return json;
}

export default formtojson;
