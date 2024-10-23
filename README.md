class_name Postava

var jmeno : String
var hp : int = 100
var zabiti : int = 0

# Konstruktor pro postavu
func _init(_jmeno: String):
    jmeno = _jmeno

# Funkce pro útok
func utok(zbran, cil):
    var poskozeni = zbran.get_poskozeni()
    cil.hp -= poskozeni
    print(jmeno + " útočí na " + cil.jmeno + " za " + str(poskozeni) + " poškození.")
    
    if cil.hp <= 0:
        cil.umri()
        return true
    return false

# Funkce pro smrt postavy
func umri():
    hp = 0
    print(jmeno + " byl zabit!")
<!---
SkibidiBrain/SkibidiBrain is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
