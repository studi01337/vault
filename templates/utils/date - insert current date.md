<%*
let result = ""
const k = ["2001-09-11","[[2001-09-11]]", "📅 2001-09-11@08:42", "#2001/09/11", "11 septembre 2001"];
const v = [0,1,2,3,4];

const format = parseInt(await tp.system.suggester(k, v, false, "format") || 0, 10);

if(format == 0) result = `${tp.date.now("YYYY-MM-DD")}`
if(format == 1) result = `[[${tp.date.now("YYYY-MM-DD")}]]`;
if(format == 2) result = `📅 ${tp.date.now("YYYY-MM-DD@HH:mm")}`;
if(format == 3) result = `#${tp.date.now("YYYY/MM/DD")}`;
if(format == 4) result = `${tp.date.now("DD MMMM YYYY")}`;

tR+=result;
-%>