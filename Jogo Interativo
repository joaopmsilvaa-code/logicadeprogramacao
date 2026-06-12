programa
{
	funcao inicio()
	{
		inteiro vidaJogador = 100
		inteiro vidaDragao = 150
		inteiro rodada = 1

		// Itens
		inteiro pocaoCura = 2
		inteiro bebidaEnergia = 2
		inteiro escudoMagico = 1
		inteiro bombaMagica = 1

		inteiro opcao
		inteiro item
		inteiro defesa = 0

		escreva("=== BATALHA CONTRA O DRAGAO ===\n")

		enquanto (vidaJogador > 0 e vidaDragao > 0)
		{
			escreva("\n============================\n")
			escreva("RODADA: ", rodada, "\n")
			escreva("Sua vida: ", vidaJogador, "\n")
			escreva("Vida do dragao: ", vidaDragao, "\n")

			escreva("\nEscolha uma acao:\n")
			escreva("1 - Atacar\n")
			escreva("2 - Defender\n")
			escreva("3 - Usar Item\n")
			leia(opcao)

			se (opcao == 1)
			{
				vidaDragao = vidaDragao - 25
				escreva("Voce atacou e causou 25 de dano!\n")
			}
			senao se (opcao == 2)
			{
				defesa = 10
				escreva("Voce entrou em modo de defesa!\n")
			}
			senao se (opcao == 3)
			{
				escreva("\nItens disponiveis:\n")
				escreva("1 - Pocao de Cura (", pocaoCura, ")\n")
				escreva("2 - Bebida Energetica (", bebidaEnergia, ")\n")
				escreva("3 - Escudo Magico (", escudoMagico, ")\n")
				escreva("4 - Bomba Magica (", bombaMagica, ")\n")

				leia(item)

				se (item == 1)
				{
					se (pocaoCura > 0)
					{
						vidaJogador = vidaJogador + 30

						se (vidaJogador > 100)
						{
							vidaJogador = 100
						}

						pocaoCura--
						escreva("Voce recuperou 30 de vida!\n")
					}
					senao
					{
						escreva("Pocao esgotada!\n")
					}
				}
				senao se (item == 2)
				{
					se (bebidaEnergia > 0)
					{
						vidaJogador = vidaJogador + 15

						se (vidaJogador > 100)
						{
							vidaJogador = 100
						}

						bebidaEnergia--
						escreva("Voce ganhou 15 de energia!\n")
					}
					senao
					{
						escreva("Bebida energetica esgotada!\n")
					}
				}
				senao se (item == 3)
				{
					se (escudoMagico > 0)
					{
						defesa = 20
						escudoMagico--
						escreva("Escudo magico ativado!\n")
					}
					senao
					{
						escreva("Escudo magico esgotado!\n")
					}
				}
				senao se (item == 4)
				{
					se (bombaMagica > 0)
					{
						vidaDragao = vidaDragao - 40
						bombaMagica--
						escreva("Bomba magica causou 40 de dano!\n")
					}
					senao
					{
						escreva("Bomba magica esgotada!\n")
					}
				}
			}

			// Ataque do dragão
			se (vidaDragao > 0)
			{
				inteiro dano = 20 - defesa

				se (dano < 0)
				{
					dano = 0
				}

				vidaJogador = vidaJogador - dano

				escreva("O dragao atacou e causou ", dano, " de dano!\n")
			}

			defesa = 0
			rodada++
		}

		escreva("\n============================\n")

		se (vidaDragao <= 0)
		{
			escreva("PARABENS! Voce derrotou o dragao e salvou o reino!\n")
		}
		senao
		{
			escreva("GAME OVER! O dragao venceu a batalha.\n")
		}
	}
}
