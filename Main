package org.example;

import java.text.Collator;
import java.util.*;

public class Main {
    public static void main(String[] args) {

        String input = "|af : Afeganistão |ax : Ilhas Aland |al : Albânia |dz : Argélia |as : Samoa Americana |ad : Andorra |ao : Angola |ai : Anguila |aq : Antártica |ag : Antígua e Barbuda |ar : Argentina |am: Armênia |aw: Aruba |au: Austrália |at: Áustria |az: Azerbaijão |bs: Bahamas |bh: Bahrein |bd: Bangladesh |bb: Barbados |por: Bielorrússia |be: Bélgica |bz: Belize | bj: Benin |bm: Bermudas |bt: Butão |bo: Bolívia |ba: Bósnia e Herzegovina |bw: Botsuana |bv: Ilha Bouvet |br: Brasil |io: Território Britânico do Oceano Índico |bn: Brunei Darussalam |bg: Bulgária |bf: Burkina Faso |bi: Burundi |kh: Camboja |cm: Camarões |ca: Canadá |cv: Cabo Verde |ky: Ilhas Cayman |cf: República Centro-Africana |td: Chade |cl: Chile |cn: China | cx: Ilha Christmas |cc: Ilhas Cocos (Keeling) |co: Colômbia |km: Comores |cg: Congo |cd: Congo, República Democrática |ck: Ilhas Cook |cr: Costa Rica |ci: Costa do Marfim |hr : Croácia |cu : Cuba |cy : Chipre |cz : República Tcheca |dk : Dinamarca |dj : Djibouti |dm : Dominica |do : República Dominicana |ec : Equador |eg : Egito |sv : El Salvador |gq : Guiné Equatorial |er: Eritreia |ee: Estônia |et: Etiópia |fk: Ilhas Falkland (Malvinas) |fo: Ilhas Faroe |fj: Fiji |fi: Finlândia |fr: França |gf: Guiana Francesa |pf: Polinésia Francesa |tf: Territórios Franceses do Sul |ga: Gabão |gm: Gâmbia |ge: Geórgia |de: Alemanha |gh: Gana |gi: Gibraltar |gr: Grécia |gl: Groenlândia |gd: Granada |gp: Guadalupe |gu: Guam |gt: Guatemala |gg: Guernsey |gn: Guiné |gw: Guiné-Bissau |gy: Guiana |ht: Haiti |hm: Ilha Heard e Ilhas Mcdonald |va: Santa Sé (Estado da Cidade do Vaticano) |hn: Honduras |hk: Hong Kong |hu: Hungria |is: Islândia |in: Índia |id: \r\n"
                + "Indonésia |ir: Irã, República Islâmica do |iq: Iraque |ie: Irlanda |im: Ilha de Man |il: Israel |it: Itália |jm: Jamaica |jp: Japão |je: Jersey |jo: Jordânia |kz: Cazaquistão |ke: Quênia |ki: Kiribati |kr: Coréia |kw: Kuwait |kg: Quirguistão |la: República Democrática Popular do Laos |lv: Letônia |lb: Líbano |ls : Lesoto |lr : Libéria |ly : Jamahiriya Árabe Líbia |li : Liechtenstein |lt : Lituânia |lu : Luxemburgo |mo : Macau |mk : Macedónia |mg : Madagáscar |mw : Malawi |my : Malásia |mv : Maldivas |ml: Mali |mt: Malta |mh: Ilhas Marshall |mq: Martinica |mr: Mauritânia |mu: Maurício |yt: Mayotte |mx: México |fm: Micronésia, Estados Federados de |md: Moldávia |mc: Mônaco |mn: Mongólia |me: Montenegro |ms: Montserrat |ma: Marrocos |mz: Moçambique |mm: Mianmar |na: Namíbia |nr: Nauru |np: Nepal |nl: Holanda |an: Antilhas Holandesas |nc: Nova Caledônia |nz: Nova Zelândia |ni: Nicarágua |ne: Níger |ng: Nigéria |nu: Niue |nf: Ilha Norfolk |mp: Ilhas Marianas do Norte |no: Noruega |om: Omã |pk: Paquistão |pw: Palau |ps : Território Palestino Ocupado |pa : Panamá |pg : Papua Nova Guiné |py : Paraguai |pe : Peru |ph : Filipinas |pn : Pitcairn |pl : Polônia |pt : Portugal |pr : Porto Rico |qa : Catar |re : Reunião |ro : Romênia |ru : Federação Russa |rw : Ruanda |bl : São Bartolomeu |sh : Santa Helena |kn : São Cristóvão e Nevis |lc : Santa Lúcia |mf : São Martinho |pm : São Pedro e Miquelon | vc: São Vicente e Granadinas |ws: Samoa |sm: São Marino |st: São Tomé e Príncipe |sa: Arábia Saudita |sn: Senegal |rs: Sérvia |sc: Seicheles |sl: Serra Leoa |sg: Singapura |sk : Eslováquia |si : Eslovênia |sb : Ilhas Salomão |so : Somália |za : África do Sul |gs : Geórgia do Sul e Ilha Sandwich. |es: Espanha |lk: Sri Lanka |sd: Sudão |sr: Suriname |sj: Svalbard e Jan Mayen |sz: Suazilândia |se: Suécia |ch: Suíça |sy: República Árabe Síria |tw: Taiwan |tj: Tajiquistão |tz : Tanzânia |th : Tailândia |tl : Timor-Leste |tg : Togo |tk : Tokelau |to : Tonga |tt : Trinidad e Tobago |tn : Tunísia |tr : Turquia |tm : Turquemenistão |tc : Turcos e Caicos Ilhas |tv: Tuvalu |ug: Uganda |ua: Ucrânia |ae: Emirados Árabes Unidos |gb: Reino Unido |us: Estados Unidos |um: Ilhas Distantes dos Estados Unidos |uy: Uruguai |uz: Uzbequistão |vu: Vanuatu |ve : Venezuela |vn : Vietnã |vg : Ilhas Virgens Britânicas |vi : Ilhas Virgens, EUA |wf : Wallis e Futuna |eh : Saara Ocidental |ye : Iêmen |zm : Zâmbia |zw : Zimbábue";

        String[] pares = input.split("\\|");
        Map<String, String> map = new HashMap<>();

        for (String par : pares) {
            String[] keyValue = par.trim().split("\\s*:\\s*");
            if(keyValue.length==2) {
                map.put(keyValue[0], keyValue[1]);
            }
        }

        List<Map.Entry<String, String>> listaAux = new ArrayList<>(map.entrySet());

        Collator collator = Collator.getInstance();
        collator.setStrength(Collator.PRIMARY);

        listaAux.sort((o1, o2) -> collator.compare(o1.getValue(), o2.getValue()));

        Map<String, String> mapOrdenado = new LinkedHashMap<>();
        for (Map.Entry<String, String> entry : listaAux) {
            mapOrdenado.put(entry.getKey(), entry.getValue());
        }

        for (Map.Entry<String, String> entry : mapOrdenado.entrySet()) {
            System.out.print(" |"+entry.getKey() + " : " + entry.getValue());
        }
    }
}
