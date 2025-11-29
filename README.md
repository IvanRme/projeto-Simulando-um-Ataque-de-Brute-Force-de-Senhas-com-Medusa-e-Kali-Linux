# Relatório de Exploração de Vulnerabilidade

---
<br>
<p align="center">
  <img src="https://img.shields.io/static/v1?label=DIO&message=Education&color=E94D5F&labelColor=202024" alt="DIO Project" />
</p>

---

<!--  -->
<table align="center">
<thead>
  <tr>
    <td>
        <p align="center">Aluno</p>
        <a href="https://github.com/marcelonascimento22">
        <img src="https://github.com/user-attachments/assets/a76b343c-fbfd-4a5a-8c87-47b43578397b" width ="300px" alt="@felipeAguiarCode"><br>
      </a>
    </td>
    <td colspan="3">
    <p> Estou me reinventando e iniciando minha carreira como Desenvolvedor, determinado a transformar minha paixão em resultados concretos e impacto positivo.
      <br/>
   
  </p>
      <a 
      href="https://www.linkedin.com/in/ivan-estudante/" 
      align="center">
           <img 
            align="center" 
            alt="Material de Apoio" 
            src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"
            >
        </a>
    </td>
  </tr>
</thead>
</table>

## 📌 1. Informações Gerais
**Título:** Relatório de Exploração de Vulnerabilidade  
**Projeto/Sistema:** Metasploitable 2 e DVWA  
**Cliente:** DIO  
**Responsáveis:** Ivan Rodrigues </br>
**Versão:** v1.0

##  2. Escopo e Regras de Engajamento
**Ambiente autorizado:**  
- Hosts/IPs: 192.168.56.102  
- Endpoints: Metasploitable 2 / VirtualBox

**Atividades:**  
- Varredura ativa  na rede
- Testes de intrusão controlados  
- Validação manual

##  3. Fases

- Reconhecimento do alvo
- Enumeração (buscar possiveis brechas no sistema)
- Análise
- Exploração 
- Evidências 
- Report

## 4. Ambiente usado
- Ambiente : Metasploitable 2 / VirtualBox

5. Ferramentas Utilizadas
- **arp-scan:** usado para descobrir todos os dispositivos ativos em uma rede local e mapear seus endereços IP e endereços físicos (MAC
- **Nmap:** serve para mapear redes, identificar dispositivos ativos e serviços, e auditar a segurança de sistemas
- **Medusa:** Ferramenta para realizar ataques de força bruta rápidos e eficientes contra diversos serviços de rede, como HTTP, FTP, SSH, Telnet, POP3, IMAP, VNC, entre outros 
- **enum4linux:** utilizada para a enumeração de informações em sistemas operacionais Windows e servidores Samba (SMB) em uma rede

  ## 📊 6. Resumo das Vulnerabilidades
| ID | Porta | Serviço| Vulnerabilidade | Severidade | Status | Observações | Versão|
|----|-------|--------|-----------------|------------|--------|-------------|-------|
| 01 | 21 | FTP | Brute Force | Crítica | Confirmada | Exposição de dados |2.3.4|
02 | 80 | HTTP | Brute Force | Crítica | Confirmada | Exposição de dados | apache httpd 2.2.8 ((ubuntu) DAV/2)
03 | 445 | SMB | Brute Force e Password Spraying | Crítica | Confirmada | Exposição de dados | SMBv1|

🕵️ 7. Vulnerabilidades detalhadas
### Exploração
**Coleta de informações relevantes:** 

**I -** Varredura da Rede com objetivo de descobrir ips que estão ativo nela.
<img align="center"  
    src="./imagens/hostativos.png"
    >
  <p>Nesse caso ,temos 3 hosts ativos, 100,101 e 102  </p>

**II -** Scaneando os serviços abertos no host alvo.
<img align="center"  
    src="./imagens/servi�oseversoes.png"
    >
## Preparando o Ataque 
   Criação das WordLists

  <p align ="center">  1-Possiveis senhas e usuarios :</p> <br>
  <img  src="./imagens/senhaseusuarios.png"
    >
