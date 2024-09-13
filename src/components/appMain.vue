<script>

import axios from 'axios';
import { store } from '../store.js'
import appSingleCard from './appSingleCard.vue';

export default {
  data() {
    return {
      store,
      searchArchetype: '',
      availableArchetypes: [
      [
        {
          archetype: "-Eyes Dragon"
        },
        {
          archetype: "\"C\""
        },
        {
          archetype: "@Ignister"
        },
        {
          archetype: "A-to-Z"
        },
        {
          archetype: "A.I."
        },
        {
          archetype: "ABC"
        },
        {
          archetype: "Abyss Actor"
        },
        {
          archetype: "Abyss Script"
        },
        {
          archetype: "Abyss-"
        },
        {
          archetype: "Adamancipator"
        },
        {
          archetype: "Advanced Crystal Beast"
        },
        {
          archetype: "Adventurer Token"
        },
        {
          archetype: "Aesir"
        },
        {
          archetype: "Aether"
        },
        {
          archetype: "Albaz Dragon"
        },
        {
          archetype: "Alien"
        },
        {
          archetype: "Alligator"
        },
        {
          archetype: "Allure Queen"
        },
        {
          archetype: "Ally of Justice"
        },
        {
          archetype: "Altergeist"
        },
        {
          archetype: "Amazement"
        },
        {
          archetype: "Amazoness"
        },
        {
          archetype: "Amorphage"
        },
        {
          archetype: "Ancient Gear"
        },
        {
          archetype: "Ancient Treasure"
        },
        {
          archetype: "Ancient Warriors"
        },
        {
          archetype: "Anotherverse"
        },
        {
          archetype: "Anti"
        },
        {
          archetype: "Apoqliphort"
        },
        {
          archetype: "Appliancer"
        },
        {
          archetype: "Aquaactress"
        },
        {
          archetype: "Aquamirror"
        },
        {
          archetype: "Arcana Force"
        },
        {
          archetype: "Archfiend"
        },
        {
          archetype: "Armed Dragon"
        },
        {
          archetype: "Aroma"
        },
        {
          archetype: "Artifact"
        },
        {
          archetype: "Ashened"
        },
        {
          archetype: "Assault Mode"
        },
        {
          archetype: "Atlantean"
        },
        {
          archetype: "Attraction"
        },
        {
          archetype: "Attribute Summoner"
        },
        {
          archetype: "Azamina"
        },
        {
          archetype: "B.E.S."
        },
        {
          archetype: "Bamboo Sword"
        },
        {
          archetype: "Barbaros"
        },
        {
          archetype: "Barian's"
        },
        {
          archetype: "Batteryman"
        },
        {
          archetype: "Battleguard"
        },
        {
          archetype: "Battlewasp"
        },
        {
          archetype: "Battlin' Boxer"
        },
        {
          archetype: "Battlin' Boxing"
        },
        {
          archetype: "Beetrooper"
        },
        {
          archetype: "Black Luster Soldier"
        },
        {
          archetype: "Blackwing"
        },
        {
          archetype: "Blaze Accelerator"
        },
        {
          archetype: "Blue Tears"
        },
        {
          archetype: "Blue-Eyes"
        },
        {
          archetype: "Bonding"
        },
        {
          archetype: "Book of"
        },
        {
          archetype: "Boot-Up"
        },
        {
          archetype: "Borrel"
        },
        {
          archetype: "Bounzer"
        },
        {
          archetype: "Branded"
        },
        {
          archetype: "Broken World"
        },
        {
          archetype: "Bugroth"
        },
        {
          archetype: "Bujin"
        },
        {
          archetype: "Burning Abyss"
        },
        {
          archetype: "Butterfly"
        },
        {
          archetype: "Butterspy"
        },
        {
          archetype: "Bystial"
        },
        {
          archetype: "Cataclysmic"
        },
        {
          archetype: "Celebration"
        },
        {
          archetype: "Celtic Guard"
        },
        {
          archetype: "Centur-Ion"
        },
        {
          archetype: "Chaos"
        },
        {
          archetype: "Chaos Phantom"
        },
        {
          archetype: "Charmer"
        },
        {
          archetype: "Chemicritter"
        },
        {
          archetype: "Chimera"
        },
        {
          archetype: "Chronomaly"
        },
        {
          archetype: "Chrysalis"
        },
        {
          archetype: "Cipher"
        },
        {
          archetype: "Circular"
        },
        {
          archetype: "Clear"
        },
        {
          archetype: "Clear Wing"
        },
        {
          archetype: "Cloudian"
        },
        {
          archetype: "Code Talker"
        },
        {
          archetype: "Codebreaker"
        },
        {
          archetype: "Constellar"
        },
        {
          archetype: "Contact"
        },
        {
          archetype: "Cosmic Synchro Monster"
        },
        {
          archetype: "Counter Fairy"
        },
        {
          archetype: "Crusadia"
        },
        {
          archetype: "Crystal"
        },
        {
          archetype: "Crystal Beast"
        },
        {
          archetype: "Crystron"
        },
        {
          archetype: "Cubic"
        },
        {
          archetype: "Cupid"
        },
        {
          archetype: "Curse of Dragon"
        },
        {
          archetype: "CXyz"
        },
        {
          archetype: "Cyber"
        },
        {
          archetype: "Cyber Angel"
        },
        {
          archetype: "Cyber Dragon"
        },
        {
          archetype: "Cyberdark"
        },
        {
          archetype: "Cynet"
        },
        {
          archetype: "D.D."
        },
        {
          archetype: "D/D"
        },
        {
          archetype: "Danger!"
        },
        {
          archetype: "Dark Contract"
        },
        {
          archetype: "Dark counterpart"
        },
        {
          archetype: "Dark Magician"
        },
        {
          archetype: "Dark Scorpion"
        },
        {
          archetype: "Dark World"
        },
        {
          archetype: "Darklord"
        },
        {
          archetype: "Deep Sea"
        },
        {
          archetype: "Demise"
        },
        {
          archetype: "Deskbot"
        },
        {
          archetype: "Despia"
        },
        {
          archetype: "Destiny HERO"
        },
        {
          archetype: "Destruction Sword"
        },
        {
          archetype: "Diabellstar"
        },
        {
          archetype: "Dice"
        },
        {
          archetype: "Digital Bug"
        },
        {
          archetype: "Dinomist"
        },
        {
          archetype: "Dinomorphia"
        },
        {
          archetype: "Dinowrestler"
        },
        {
          archetype: "Divine Dragon"
        },
        {
          archetype: "Djinn"
        },
        {
          archetype: "Dododo"
        },
        {
          archetype: "Dogmatika"
        },
        {
          archetype: "Doll"
        },
        {
          archetype: "Doll Monster"
        },
        {
          archetype: "Doodle Beast"
        },
        {
          archetype: "Doodlebook"
        },
        {
          archetype: "Doriado"
        },
        {
          archetype: "Draconia"
        },
        {
          archetype: "Dracoslayer"
        },
        {
          archetype: "Dracoverlord"
        },
        {
          archetype: "Dragonmaid"
        },
        {
          archetype: "Dragunity"
        },
        {
          archetype: "Dream Mirror"
        },
        {
          archetype: "Drytron"
        },
        {
          archetype: "Dual Avatar"
        },
        {
          archetype: "Duston"
        },
        {
          archetype: "Earthbound"
        },
        {
          archetype: "Edge Imp"
        },
        {
          archetype: "Egyptian God"
        },
        {
          archetype: "Eldlich"
        },
        {
          archetype: "Elemental HERO"
        },
        {
          archetype: "Elemental Lord"
        },
        {
          archetype: "Elementsaber"
        },
        {
          archetype: "Emblema"
        },
        {
          archetype: "Empower"
        },
        {
          archetype: "Empowered Warrior"
        },
        {
          archetype: "Endymion"
        },
        {
          archetype: "Evil Eye"
        },
        {
          archetype: "Evil HERO"
        },
        {
          archetype: "Evil★Twin"
        },
        {
          archetype: "Evol"
        },
        {
          archetype: "Evolsaur"
        },
        {
          archetype: "Evoltile"
        },
        {
          archetype: "Evolzar"
        },
        {
          archetype: "Exchange of the Spirit"
        },
        {
          archetype: "Exodd"
        },
        {
          archetype: "Exodia"
        },
        {
          archetype: "Exosister"
        },
        {
          archetype: "Eyes Restrict"
        },
        {
          archetype: "F.A."
        },
        {
          archetype: "Fabled"
        },
        {
          archetype: "Fairy"
        },
        {
          archetype: "Fairy Tail"
        },
        {
          archetype: "Favorite"
        },
        {
          archetype: "Felgrand"
        },
        {
          archetype: "Field Searcher"
        },
        {
          archetype: "Fiendsmith"
        },
        {
          archetype: "Fire Fist"
        },
        {
          archetype: "Fire Formation"
        },
        {
          archetype: "Fire King"
        },
        {
          archetype: "Firewall"
        },
        {
          archetype: "Fishborg"
        },
        {
          archetype: "Flame Swordsman"
        },
        {
          archetype: "Flamvell"
        },
        {
          archetype: "Fleur"
        },
        {
          archetype: "Floowandereeze"
        },
        {
          archetype: "Flower Cardian"
        },
        {
          archetype: "Fluffal"
        },
        {
          archetype: "Forbidden"
        },
        {
          archetype: "Fortune Fairy"
        },
        {
          archetype: "Fortune Lady"
        },
        {
          archetype: "Fossil"
        },
        {
          archetype: "Frightfur"
        },
        {
          archetype: "Frog"
        },
        {
          archetype: "From the Underworld"
        },
        {
          archetype: "Fur Hire"
        },
        {
          archetype: "Fusion"
        },
        {
          archetype: "G Golem"
        },
        {
          archetype: "Gadget"
        },
        {
          archetype: "Gagaga"
        },
        {
          archetype: "Gaia Knight"
        },
        {
          archetype: "Gaia The Fierce Knight"
        },
        {
          archetype: "Galaxy"
        },
        {
          archetype: "Galaxy-Eyes"
        },
        {
          archetype: "Gandora"
        },
        {
          archetype: "Gate Guardian"
        },
        {
          archetype: "Geargia"
        },
        {
          archetype: "Gem-"
        },
        {
          archetype: "Generaider"
        },
        {
          archetype: "Genex"
        },
        {
          archetype: "Ghostrick"
        },
        {
          archetype: "Ghoti"
        },
        {
          archetype: "Gimmick Puppet"
        },
        {
          archetype: "Gishki"
        },
        {
          archetype: "Gizmek"
        },
        {
          archetype: "Glacial Beast"
        },
        {
          archetype: "Gladiator Beast"
        },
        {
          archetype: "Goblin"
        },
        {
          archetype: "Gogogo"
        },
        {
          archetype: "Gold Pride"
        },
        {
          archetype: "Golden Castle of Stromberg"
        },
        {
          archetype: "Golden Land"
        },
        {
          archetype: "Gorgonic"
        },
        {
          archetype: "Gouki"
        },
        {
          archetype: "GranSolfachord"
        },
        {
          archetype: "Gravekeeper's"
        },
        {
          archetype: "Graydle"
        },
        {
          archetype: "Greed"
        },
        {
          archetype: "Grepher"
        },
        {
          archetype: "Guardian"
        },
        {
          archetype: "Guardragon"
        },
        {
          archetype: "Gunkan"
        },
        {
          archetype: "Gusto"
        },
        {
          archetype: "Harpie"
        },
        {
          archetype: "Hazy"
        },
        {
          archetype: "Heart"
        },
        {
          archetype: "Herald"
        },
        {
          archetype: "Heraldic"
        },
        {
          archetype: "Heraldry"
        },
        {
          archetype: "HERO"
        },
        {
          archetype: "Heroic"
        },
        {
          archetype: "Hi-Speedroid"
        },
        {
          archetype: "Hieratic"
        },
        {
          archetype: "Hole"
        },
        {
          archetype: "Holy Knight"
        },
        {
          archetype: "Horus"
        },
        {
          archetype: "Horus the Black Flame Dragon"
        },
        {
          archetype: "Hyperion"
        },
        {
          archetype: "Ice Barrier"
        },
        {
          archetype: "Icejade"
        },
        {
          archetype: "Igknight"
        },
        {
          archetype: "Impcantation"
        },
        {
          archetype: "Infernity"
        },
        {
          archetype: "Infernoble Arms"
        },
        {
          archetype: "Infernoble Knight"
        },
        {
          archetype: "Infernoid"
        },
        {
          archetype: "Infestation"
        },
        {
          archetype: "Infinitrack"
        },
        {
          archetype: "Invoked"
        },
        {
          archetype: "Inzektor"
        },
        {
          archetype: "Iron Chain"
        },
        {
          archetype: "Jar"
        },
        {
          archetype: "Jester"
        },
        {
          archetype: "Jinzo"
        },
        {
          archetype: "Junk"
        },
        {
          archetype: "Jurrac"
        },
        {
          archetype: "Kaiju"
        },
        {
          archetype: "Kairyu-Shin"
        },
        {
          archetype: "Karakuri"
        },
        {
          archetype: "Kashtira"
        },
        {
          archetype: "Ki-sikil"
        },
        {
          archetype: "Knight"
        },
        {
          archetype: "Knightmare"
        },
        {
          archetype: "Koa'ki Meiru"
        },
        {
          archetype: "Koala"
        },
        {
          archetype: "Kozmo"
        },
        {
          archetype: "Krawler"
        },
        {
          archetype: "Kuriboh"
        },
        {
          archetype: "Labrynth"
        },
        {
          archetype: "Labyrinth Wall"
        },
        {
          archetype: "Lady of Lament"
        },
        {
          archetype: "Laval"
        },
        {
          archetype: "Legendary Knight"
        },
        {
          archetype: "Libromancer"
        },
        {
          archetype: "Light and Darkness Dragon"
        },
        {
          archetype: "Lightsworn"
        },
        {
          archetype: "Lil-la"
        },
        {
          archetype: "Live☆Twin"
        },
        {
          archetype: "Lswarm"
        },
        {
          archetype: "Lunalight"
        },
        {
          archetype: "Lyrilusc"
        },
        {
          archetype: "M∀LICE"
        },
        {
          archetype: "Machina"
        },
        {
          archetype: "Machine Angel"
        },
        {
          archetype: "Madolche"
        },
        {
          archetype: "Madoor"
        },
        {
          archetype: "Magical Musket"
        },
        {
          archetype: "Magician"
        },
        {
          archetype: "Magician Girl"
        },
        {
          archetype: "Magikey"
        },
        {
          archetype: "Magistus"
        },
        {
          archetype: "Magnet Warrior"
        },
        {
          archetype: "Majespecter"
        },
        {
          archetype: "Majestic"
        },
        {
          archetype: "Maju"
        },
        {
          archetype: "Malefic"
        },
        {
          archetype: "Malicevorous"
        },
        {
          archetype: "Maliss"
        },
        {
          archetype: "Man-Eater Bug"
        },
        {
          archetype: "Mannadium"
        },
        {
          archetype: "Marincess"
        },
        {
          archetype: "Martial Art Spirit"
        },
        {
          archetype: "Mask"
        },
        {
          archetype: "Masked HERO"
        },
        {
          archetype: "Materiactor"
        },
        {
          archetype: "Mathmech"
        },
        {
          archetype: "Mayakashi"
        },
        {
          archetype: "Mecha Phantom Beast"
        },
        {
          archetype: "Megalith"
        },
        {
          archetype: "Mekk-Knight"
        },
        {
          archetype: "Meklord"
        },
        {
          archetype: "Melffy"
        },
        {
          archetype: "Melodious"
        },
        {
          archetype: "Memento"
        },
        {
          archetype: "Mermail"
        },
        {
          archetype: "Metalfoes"
        },
        {
          archetype: "Metalmorph"
        },
        {
          archetype: "Metaphys"
        },
        {
          archetype: "Mikanko"
        },
        {
          archetype: "Millennium"
        },
        {
          archetype: "Mimighoul"
        },
        {
          archetype: "Mirror Trap"
        },
        {
          archetype: "Mist Valley"
        },
        {
          archetype: "Mokey Mokey"
        },
        {
          archetype: "Monarch"
        },
        {
          archetype: "Morganite"
        },
        {
          archetype: "Morphtronic"
        },
        {
          archetype: "Mulcharmy"
        },
        {
          archetype: "Mystical Beast of the Forest"
        },
        {
          archetype: "Mythical Beast"
        },
        {
          archetype: "Myutant"
        },
        {
          archetype: "Naturia"
        },
        {
          archetype: "Nekroz"
        },
        {
          archetype: "Nemeses"
        },
        {
          archetype: "Nemleria"
        },
        {
          archetype: "Nemurelia"
        },
        {
          archetype: "Neo Space"
        },
        {
          archetype: "Neo-Spacian"
        },
        {
          archetype: "Neos"
        },
        {
          archetype: "Nephthys"
        },
        {
          archetype: "Nimble"
        },
        {
          archetype: "Ninja"
        },
        {
          archetype: "Ninjitsu Art"
        },
        {
          archetype: "Noble Arms"
        },
        {
          archetype: "Noble Knight"
        },
        {
          archetype: "Nordic"
        },
        {
          archetype: "Nouvelles"
        },
        {
          archetype: "Number"
        },
        {
          archetype: "Numeron"
        },
        {
          archetype: "Odd-Eyes"
        },
        {
          archetype: "Ogdoadic"
        },
        {
          archetype: "Ojama"
        },
        {
          archetype: "Onomat"
        },
        {
          archetype: "Orcust"
        },
        {
          archetype: "Overlay"
        },
        {
          archetype: "P.U.N.K."
        },
        {
          archetype: "Paladins of Dragons"
        },
        {
          archetype: "Paleozoic"
        },
        {
          archetype: "Parasite"
        },
        {
          archetype: "Parshath"
        },
        {
          archetype: "Patissciel"
        },
        {
          archetype: "Pendulum"
        },
        {
          archetype: "Pendulum Dragon"
        },
        {
          archetype: "Penguin"
        },
        {
          archetype: "Performage"
        },
        {
          archetype: "Performapal"
        },
        {
          archetype: "Phantasm"
        },
        {
          archetype: "Phantasm Spiral"
        },
        {
          archetype: "Phantom Knights"
        },
        {
          archetype: "Photon"
        },
        {
          archetype: "Plunder Patroll"
        },
        {
          archetype: "Polymerization"
        },
        {
          archetype: "Possessed"
        },
        {
          archetype: "Potan"
        },
        {
          archetype: "Power Tool"
        },
        {
          archetype: "Prank-Kids"
        },
        {
          archetype: "Predap"
        },
        {
          archetype: "Predaplant"
        },
        {
          archetype: "Prediction Princess"
        },
        {
          archetype: "Priestess"
        },
        {
          archetype: "Primoredial"
        },
        {
          archetype: "Prophecy"
        },
        {
          archetype: "PSY-Frame"
        },
        {
          archetype: "Puppet"
        },
        {
          archetype: "Purrely"
        },
        {
          archetype: "Qli"
        },
        {
          archetype: "Ragnaraika"
        },
        {
          archetype: "Raidraptor"
        },
        {
          archetype: "Rainbow Bridge"
        },
        {
          archetype: "Raizeol"
        },
        {
          archetype: "Rank-Up-Magic"
        },
        {
          archetype: "Recipe"
        },
        {
          archetype: "Red-Eyes"
        },
        {
          archetype: "Relinquished"
        },
        {
          archetype: "Reptilianne"
        },
        {
          archetype: "Rescue Squad"
        },
        {
          archetype: "Rescue-ACE"
        },
        {
          archetype: "Resonator"
        },
        {
          archetype: "Rikka"
        },
        {
          archetype: "Risebell"
        },
        {
          archetype: "Ritual Beast"
        },
        {
          archetype: "Roid"
        },
        {
          archetype: "Rokket"
        },
        {
          archetype: "Roland"
        },
        {
          archetype: "Rose"
        },
        {
          archetype: "Rose Dragon"
        },
        {
          archetype: "Runick"
        },
        {
          archetype: "Ryu-Ge"
        },
        {
          archetype: "Ryzeal"
        },
        {
          archetype: "S-Force"
        },
        {
          archetype: "Saber"
        },
        {
          archetype: "Sacred Beast"
        },
        {
          archetype: "Salamandra"
        },
        {
          archetype: "Salamangreat"
        },
        {
          archetype: "Sangen"
        },
        {
          archetype: "Scareclaw"
        },
        {
          archetype: "Schoolwork Success"
        },
        {
          archetype: "Scrap"
        },
        {
          archetype: "Scrap-Iron"
        },
        {
          archetype: "Sea Stealth"
        },
        {
          archetype: "Secret Six Samurai"
        },
        {
          archetype: "Seventh"
        },
        {
          archetype: "Shaddoll"
        },
        {
          archetype: "Shark"
        },
        {
          archetype: "Shining Sarcophagus"
        },
        {
          archetype: "Shinobird"
        },
        {
          archetype: "Shiranui"
        },
        {
          archetype: "Signature move"
        },
        {
          archetype: "Silent Magician"
        },
        {
          archetype: "Silent Swordsman"
        },
        {
          archetype: "Simorgh"
        },
        {
          archetype: "Sinful Spoils"
        },
        {
          archetype: "Six Samurai"
        },
        {
          archetype: "Six Strike"
        },
        {
          archetype: "Skilled Magician"
        },
        {
          archetype: "Skull Servant"
        },
        {
          archetype: "Sky Scourge"
        },
        {
          archetype: "Sky Striker"
        },
        {
          archetype: "Slime"
        },
        {
          archetype: "Snake-Eye"
        },
        {
          archetype: "Solemn"
        },
        {
          archetype: "Solfachord"
        },
        {
          archetype: "Speedroid"
        },
        {
          archetype: "Spellbook"
        },
        {
          archetype: "Sphinx"
        },
        {
          archetype: "Spider"
        },
        {
          archetype: "Spirit Message"
        },
        {
          archetype: "Spiritual Art"
        },
        {
          archetype: "Spright"
        },
        {
          archetype: "Springans"
        },
        {
          archetype: "SPYRAL"
        },
        {
          archetype: "Star"
        },
        {
          archetype: "Star Seraph"
        },
        {
          archetype: "Stardust"
        },
        {
          archetype: "Starliege"
        },
        {
          archetype: "Starry Knight"
        },
        {
          archetype: "Stealth Kragen"
        },
        {
          archetype: "Steelswarm"
        },
        {
          archetype: "Stellarknight"
        },
        {
          archetype: "Subterror"
        },
        {
          archetype: "Sunavalon"
        },
        {
          archetype: "Sunseed"
        },
        {
          archetype: "Sunvine"
        },
        {
          archetype: "Super Defense Robot"
        },
        {
          archetype: "Super Quant"
        },
        {
          archetype: "Superheavy"
        },
        {
          archetype: "Superheavy Samurai"
        },
        {
          archetype: "Supreme King"
        },
        {
          archetype: "Swarm of"
        },
        {
          archetype: "Swordsoul"
        },
        {
          archetype: "Sylvan"
        },
        {
          archetype: "Symphonic Warrior"
        },
        {
          archetype: "Synchro"
        },
        {
          archetype: "Synchron"
        },
        {
          archetype: "T.G."
        },
        {
          archetype: "Tachyon"
        },
        {
          archetype: "Tearlaments"
        },
        {
          archetype: "Tellarknight"
        },
        {
          archetype: "Tenpai Dragon"
        },
        {
          archetype: "Tenyi"
        },
        {
          archetype: "The Agent"
        },
        {
          archetype: "The Sanctuary in the Sky"
        },
        {
          archetype: "The Weather"
        },
        {
          archetype: "Therion"
        },
        {
          archetype: "Thunder Dragon"
        },
        {
          archetype: "Time Thief"
        },
        {
          archetype: "Timelord"
        },
        {
          archetype: "Tindangle"
        },
        {
          archetype: "Tistina"
        },
        {
          archetype: "Toon"
        },
        {
          archetype: "Toy"
        },
        {
          archetype: "Train"
        },
        {
          archetype: "Transcendosaurus"
        },
        {
          archetype: "Trap Hole"
        },
        {
          archetype: "Trap Monster"
        },
        {
          archetype: "Traptrix"
        },
        {
          archetype: "Tri-Brigade"
        },
        {
          archetype: "Triamid"
        },
        {
          archetype: "Trickstar"
        },
        {
          archetype: "True Draco"
        },
        {
          archetype: "U.A."
        },
        {
          archetype: "Umbral Horror"
        },
        {
          archetype: "Umi"
        },
        {
          archetype: "Unchained"
        },
        {
          archetype: "Underworld"
        },
        {
          archetype: "Uniform Nomenclature"
        },
        {
          archetype: "Ursarctic"
        },
        {
          archetype: "Utopia"
        },
        {
          archetype: "Utopic"
        },
        {
          archetype: "Vaalmonica"
        },
        {
          archetype: "Valkyrie"
        },
        {
          archetype: "Vampire"
        },
        {
          archetype: "Vanquish Soul"
        },
        {
          archetype: "Vassal"
        },
        {
          archetype: "Vaylantz"
        },
        {
          archetype: "Veda"
        },
        {
          archetype: "Vendread"
        },
        {
          archetype: "Venom"
        },
        {
          archetype: "Vernusylph"
        },
        {
          archetype: "Virtual World"
        },
        {
          archetype: "Visas"
        },
        {
          archetype: "Vision HERO"
        },
        {
          archetype: "Voiceless Voice"
        },
        {
          archetype: "Void"
        },
        {
          archetype: "Volcanic"
        },
        {
          archetype: "Vylon"
        },
        {
          archetype: "War Rock"
        },
        {
          archetype: "Watt"
        },
        {
          archetype: "Wedju"
        },
        {
          archetype: "White"
        },
        {
          archetype: "White Forest"
        },
        {
          archetype: "Wicked God"
        },
        {
          archetype: "Wight"
        },
        {
          archetype: "Wind-Up"
        },
        {
          archetype: "Windwitch"
        },
        {
          archetype: "Witchcrafter"
        },
        {
          archetype: "with Eyes of Blue"
        },
        {
          archetype: "World Chalice"
        },
        {
          archetype: "World Legacy"
        },
        {
          archetype: "Worm"
        },
        {
          archetype: "X-Saber"
        },
        {
          archetype: "Xyz"
        },
        {
          archetype: "Yang Zing"
        },
        {
          archetype: "Yosenju"
        },
        {
          archetype: "Yubel"
        },
        {
          archetype: "Zefra"
        },
        {
          archetype: "Zera"
        },
        {
          archetype: "Zexal"
        },
        {
          archetype: "Zombie counterpart"
        },
        {
          archetype: "Zoodiac"
        }
]
      ],
      fullURL: 'https://db.ygoprodeck.com/api/v7/cardinfo.php',
    }
  },
  components: {
    appSingleCard
  },
  created() {
    
  },
  methods: {
    performSearch() {

      axios
      .get(this.fullURL, {
        params: {
          archetype: this.searchArchetype,
        }
      })
      .then((res) => {
        this.store.allCards = res.data.data; 
      }
    ) 
    }
  }
}
</script>

<!-- All'interno del template ci va un solo elemento -->
<template> 
  <main>
    <div class="container">
      <div class="row">
        <div class="col py-3">
          <select v-model="searchArchetype"  class="form-select" aria-label="Select">
            <option value="" selected>Select Archetype</option>
            <option v-for="(archetype, index) in availableArchetypes" :key="index" :value="availableArchetypes.archetype" @click="performSearch()">
              {{ availableArchetypes.archetype }}
            </option>
          </select>
        </div>
        <div class="general-container">
          <div class="row cards-found fw-bold text-white d-flex align-items-center px-3">
            Found X cards
          </div>
          <div class="card-container w-100 py-5">
            <appSingleCard v-for="(card, index) in store.allCards" :key="index" :myCardName="card.name" :myCardImage="card.card_images[0].image_url" :myCardArchetype="card.archetype" />
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
  main {
    height: calc(100% - 75px);
    width: 100%;
    background-color: $myOrange;

    .form-select {
      width: 150px;

      &:hover {
        cursor: pointer;
      }
    }

    .general-container {
      padding: 50px 25px;
      background-color: white;
      margin-bottom: 50px;

      .cards-found {
        height: 75px;
        background-color: black;
        margin: 0;
      }

      .card-container {
        display: flex;
        flex-wrap: wrap;    
      }
    }
  }

</style>
