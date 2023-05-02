<%*
let input = (await tp.system.clipboard() || '').trim()
if(!/\d{4}-\d{2}-\d{2}/.test(input)) return

const ts = moment(input).unix()
%><% ts %>