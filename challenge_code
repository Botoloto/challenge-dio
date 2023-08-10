extrato = []
LIMITE_SAQUE = 3
limite_transacao = 500
saldo = 0
mensagem = ''


while True:
    escolha = int(input('----- [ Bem vindo ] ----- \n\n 1) - Saque \n 2) - Depósito \n 3) - Extrato \n 4) - Sair \n\nEscolha uma opção...:\n\n'))
    if escolha == 1:
        print('\n--- [ Saque ] ---')
        if LIMITE_SAQUE > 0:
            valor = float(input('\nQuanto deseja sacar?\n'))
            if valor < 500:
                if saldo >= valor:
                    saldo -= valor
                    LIMITE_SAQUE -= 1
                    mensagem = f'[ Saque realizado ] - Novo saldo: R$ {saldo:.2f}'
                    extrato.append(mensagem)
                    print(f'\n{mensagem}')
                else:
                    mensagem = f'[ ERRO ] - Saldo indisponivel (Atual: R$ {saldo:.2f})'
                    extrato.append(mensagem)
                    print(f'\n{mensagem}')
            else:  
                mensagem = '[ ERRO ] - Valor acima de R$ 500.00'
                extrato.append(mensagem)
                print(f'\n{mensagem}')
        else:
            mensagem = '[ ERRO ] - Limite diario de 3 transações ja atingidos'
            extrato.append(mensagem)
            print(f'\n{mensagem}')
            break
    elif escolha == 2:
        print('\n--- [ Depósito ] ---')
        valor = int(input('\nQuanto deseja depositar?\n'))
        if valor > 0:
            saldo += valor
            mensagem = f'[ Depósito realizado ] - Novo saldo: R$ {saldo:.2f}'
            extrato.append(mensagem)
            print(f'\n{mensagem}')
        else:
            mensagem = f'[ ERRO ] - Valor negativo (R$ {valor:.2f})'
            extrato.append(mensagem)
            print(f'\n{mensagem}')
    elif escolha == 3:
        print('\n--- [ Extrato ] ---')
        for msg in extrato:
            print(msg)
    else:
        print('\n--- [ Saindo... ] ---')
        break
    
