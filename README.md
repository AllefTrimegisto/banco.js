# banco.js
let Banco = {
    conta: 123456,
    saldo: 0,
    tipoDeConta: "Corrente",
    agencia: "1234",
    buscarSaldo: function(){
        return this.saldo;
    },
    deposito: function(valor){
        this.saldo += valor;
    },
    saque: function(valor){
        this.saldo -= valor;
    },
    numeroDaConta: function(){
        return this.conta;
    }
};
console.log("Saldo: "+ Banco.buscarSaldo());
Banco.deposito(1000);
console.log("Saldo: "+ Banco.buscarSaldo());
Banco.saque(500);
console.log("Saldo: "+ Banco.buscarSaldo());
console.log("Numero da conta: "+ Banco.numeroDaConta());
