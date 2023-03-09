<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/css/bootstrap.min.css"
 integrity="sha384-TX8t27EcRE3e/ihU7zmQxVncDAy5uIKz4rEkgIXeMed4M0jlfIDPvg6uqKI2xXr2" 
crossorigin="anonymous">
<style>
    .container {
    background-color: lightgray;
    padding: 50px;
    outline: 3px dashed #000000;
    outline-offset: -30px;
    text-align: ;
}
input[type=submit] {
    padding: 8px 50px;
    background: #2286c9;
    border: 0;
    outline: none;
    cursor: pointer;
    font-size: 15px;
    font-weight: 500;
    border-radius: 30px;
    color: aliceblue;
}
span[class="required"] {
    color: #da0606;
}
.loader{
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    display: flex;
    justify-content:  center;
    align-items: center;
    background-color: #f7f9fb;
    transition: opacity 0.75s, visibility 0.75s;
}

.loader-hidden{
    opacity: 0;
    visibility: hidden;
}

.loader::after{
    content: "";
    width: 75px;
    height: 75px;
    border: 15px solid #dddddd;
    border-top-color: #7449f5;
    border-radius: 50%;
    animation: loading 0.7s ease infinite;
}

@keyframes loading {
    from{
        transform: rotate(0turn);
    }
    to{
        transform: rotate(1turn);
    }
}

</style>

</head>
<body>
    <div class="container">
        <div class="row">
            <div class="col">         
                <form name="submit-to-google-sheet">
                                    <center><img src="https://drive.google.com/uc?export=view&id=1WTcS6yQoFEWiXVsTmJoqjHzmGzNMnjc4" width="200px" height="auto" alt="image"></center>
                                    <p class="h4 mb-4 text-center">Borang Tempahan Bilik Mesyuarat</p>
        
                                    <div class="form-row">
                                        <div class="form-group col-md-6">
                                            <label for="first_name">Nama Pemohon:</label>
                                            <span class="required">*</span>
                                            <input type="text" class="form-control" id="first_name" name="Nama Pemohon" placeholder="" required 
                                            oninvalid="setCustomValidity('Sila isi bahagian ini')"
                                            oninput="setCustomValidity('')" />
                                        </div>
                                        <div class="form-group col-md-6">
                                            <label for="last_name">Cawangan/Unit:</label>
                                            <input type="text" class="form-control" id="last_name" name="Cawangan/Unit" placeholder="">
                                        </div>
                                    </div>
                                    <div class="form-row">
                                        
                                        <div class="form-group col-md-6">
                                            <label for="phone">No. Tel.:</label>
                                            <span class="required">*</span>
                                            <input type="tel" class="form-control" id="phone" name="No.Tel" placeholder="019xxxxxxx" required 
                                            oninvalid="setCustomValidity('Sila isi bahagian ini')"
                                            oninput="setCustomValidity('')" />
                                        </div> 
                                        <div class="form-group col-md-6">
                                            <label for="email">E-mail:</label>
                                            <span class="required">*</span>
                                            <input type="email" class="form-control" id="email" name="E-mail" placeholder="" required 
                                            oninvalid="setCustomValidity('Sila isi bahagian ini')"
                                            oninput="setCustomValidity('')" />
                                        </div>      
                                    </div>

                                    <div class="form-row">
                                        <div class="form-group col-md-6">
                                            <label for="dateOfBirth">Tarikh:</label>
                                            <span class="required">*</span>
                                            <input type="date" class="form-control" id="dateOfBirth" name="Tarikh" required 
                                            oninvalid="setCustomValidity('Sila isi bahagian ini')"
                                            oninput="setCustomValidity('')" />
                                        </div>
                                        <div class="form-group col-md-6">
                                            <label for="last_name">Bilik mesyuarat yang ingin ditempah:</label>
                                            <span class="required">*</span><br>
                                            <select class="form-control col-md-3" aria-label=".form-select-lg example" name="Bilik Mesyuarat" id="BM" required 
                                            oninvalid="setCustomValidity('Sila isi bahagian ini')"
                                            oninput="setCustomValidity('')" />
                                                <option value="BM1">BM1</option>
                                                <option value="BM2">BM2</option>
                                                <option value="BM3">BM3</option>
                                                <option value="BM4">BM4</option>
                                            </select>
                                        </div>
                                    </div>   
                                    <div class="form-row">
                                        <div class="form-group col-md-6">
                                            <label for="last_name">Waktu Mula:</label>
                                            <span class="required">*</span>
                                            <input type="time" class="form-control" id="time" name="Waktu Mula" placeholder="" required 
                                            oninvalid="setCustomValidity('Sila isi bahagian ini')"
                                            oninput="setCustomValidity('')" />
                                        </div>
                                        <div class="form-group col-md-6">
                                            <label for="first_name">Tajuk Mesyuarat/ Taklimat/ Kursus/ Bengkel:</label>
                                            <span class="required">*</span>
                                            <input type="text" class="form-control" id="first_name" name="Tajuk Mesyuarat/ Taklimat/ Kursus/ Bengkel" placeholder="" required 
                                            oninvalid="setCustomValidity('Sila isi bahagian ini')"
                                            oninput="setCustomValidity('')" />
                                        </div>           
                                    </div>
                                    <div class="form-row">
                                        <div class="form-group col-md-6">
                                            <label for="last_name">Waktu Selesai:</label>
                                            <span class="required">*</span>
                                            <input type="time" class="form-control" id="time" name="Waktu Selesai" placeholder="" required 
                                            oninvalid="setCustomValidity('Sila isi bahagian ini')"
                                            oninput="setCustomValidity('')" />
                                        </div>
                                        <div class="form-group col-md-6">
                                            <label for="last_name">lain-lain keperluan tambahan yang diperlukan(Nyatakan):</label>
                                            <input type="text" class="form-control" id="lain" name="lain" placeholder="Cth: Komputer Riba, Papan Putih, Projektor LCD/DLP">
                                        </div>
                                    </div>
                                     <br>                     
                    <center><input type="submit" name="submit" value="Hantar"></center><br>
                    <center><span id="success" style="color: aliceblue; background-color: #14bd76;"></span></center>
                    <div class="loader"></div>
                </form>
            </div>
        </div>
    </div>
    
    <script>
        const scriptURL = 'https://script.google.com/macros/s/AKfycbzMECehmTRJ1_gmWK9K0Ol_LKcUh0LRTew5KMLc7LCslcVvo-UPbToHeyrsodWgHpFPwA/exec'
        const form = document.forms['submit-to-google-sheet']
        const success = document.getElementById('success');
        form.addEventListener('submit', e => {
            e.preventDefault()
            fetch(scriptURL, { method: 'POST', body: new FormData(form)})
                .then(response => {
                success.innerHTML="_Borang Anda Telah Berjaya Dihantar! kami akan hubungi anda dalam masa terdekat TERIMA KASIH!_";

                setTimeout(function()
                {
                    success.innerHTML=""
                },8000)
                form.reset();
            })
            .catch(error => console.error('Error!', error.message))
        })
        window.addEventListener("load", () => {
            const loader = document.querySelector(".loader");

            loader.classList.add("loader-hidden");

            loader.addEventListener("transtionernd", () => {
                document.body.removeChild("loader");
            })
        })
    </script>      
</body>
</html>
