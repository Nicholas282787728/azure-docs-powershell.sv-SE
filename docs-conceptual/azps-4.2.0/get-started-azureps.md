---
title: Komma igång med Azure PowerShell
description: ''
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 04/24/2020
ms.openlocfilehash: c0b8ab83052bbe069abe170955f9409eca2118d6
ms.sourcegitcommit: 5523170e571fbd1dc93bd0fa4223aba3b324d3b0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/25/2020
ms.locfileid: "85363560"
---
# <a name="get-started-with-azure-powershell"></a>Komma igång med Azure PowerShell

Azure PowerShell är utformat för att hantera och administrera Azure-resurser från kommandoraden.
Använd Azure PowerShell när du vill skapa automatiserade verktyg som använder Azure Resource Manager-modellen. Prova det i webbläsaren med [Azure Cloud Shell](/azure/cloud-shell/overview) eller installera det på din lokala dator.

Den här artikeln hjälper dig att komma igång med Azure PowerShell och du får lära dig grundbegreppen.

## <a name="install-or-run-in-azure-cloud-shell"></a>Installera eller köra i Azure Cloud Shell

Det enklaste sättet att komma igång med Azure PowerShell är att prova det i en miljö med Azure Cloud Shell. Läs i [Snabbstart för PowerShell i Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell) för att komma igång. Cloud Shell kör PowerShell på en Linux-container, så Windows-specifika funktioner är inte tillgängliga.

När du är redo att installera Azure PowerShell på din lokala dator följer du anvisningarna i [Installera Azure PowerShell-modulen](install-az-ps.md).

## <a name="sign-in-to-azure"></a>Logga in på Azure

Logga in interaktivt med [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount)-cmdleten. Hoppa över det här steget om du använder Cloud Shell. Azure Cloud Shell-sessionen har redan autentiserats för den miljö, prenumeration och klientorganisation som Cloud Shell-sessionen startades från.

```azurepowershell-interactive
Connect-AzAccount
```

Azures molntjänster erbjuder miljöer som följer regionala lagar för datahantering. För konton i ett regionalt moln använder du parametern **Environment** för att logga in. Hämta namnet på miljön för din region med cmdleten [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment).
Exempel: För att logga in på Azure Kina 21Vianet:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

I Windows PowerShell 5.1-miljöer visas en inloggningsdialogruta där du kan ange användarnamn och lösenord för ditt Azure-konto. I alla andra versioner av PowerShell får du en token som du kan använda på [microsoft.com/devicelogin](https://microsoft.com/devicelogin). Öppna den här sidan i webbläsaren och ange token. Logga sedan in med dina Azure-autentiseringsuppgifter och auktorisera Azure PowerShell.

Efter att du loggat in ser du information om vilka av dina Azure-prenumerationer som är aktiva. Om du har flera Azure-prenumerationer i ditt konto och vill välja en annan, hämtar du dina tillgängliga prenumerationer med [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) och använder cmdleten [Set-AzContext](/powershell/module/az.accounts/set-azcontext) med ditt prenumerations-ID. Mer information om hur du hanterar dina Azure-prenumerationer i Azure PowerShell finns i [Använda flera Azure-prenumerationer](manage-subscriptions-azureps.md).

När du är inloggad på ett Azure-konto kan du använda Azure PowerShell-cmdletar för att komma åt och hantera resurserna i prenumerationen. Läs mer om inloggningsprocess och autentiseringsmetoder i [Logga in med Azure PowerShell](authenticate-azureps.md).

## <a name="find-commands"></a>Hitta kommandon

Azure PowerShell-cmdletarna följer en standardkonvention för namngivning i PowerShell, `Verb-Noun`. Verbet beskriver åtgärden (till exempel `New`, `Get`, `Set`, `Remove`) och substantivet beskriver resurstypen (till exempel `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`). Substantiv i Azure PowerShell börjar alltid med prefixet `Az`. En fullständig lista över standardverb finns i [Godkända verb för PowerShell-kommandon](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands).

Att känna till vilka substantiv, verb och Azure PowerShell-moduler som är tillgängliga hjälper dig att hitta kommandon med cmdleten [Get-Command](/powershell/module/microsoft.powershell.core/get-command). Exempel: Om du vill hitta alla VM-relaterade kommandon som använder verbet `Get`:

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

Som hjälp för dig att hitta vanliga kommandon finns här en tabell med resurstyp, motsvarande Azure PowerShell-modulen och de substantivprefix som ska användas med `Get-Command`:

|                              Resurstyp                              |                   Azure PowerShell-modul                    |    Substantivprefix     |
| ----------------------------------------------------------------------- | ------------------------------------------------------------ | ------------------ |
| [Resursgrupp](/azure/azure-resource-manager/resource-group-overview) | [Az.Resources](/powershell/module/az.resources#resources)    | `AzResourceGroup`  |
| [Virtuella datorer](/azure/virtual-machines)                             | [Az.Compute](/powershell/module/az.compute#virtual_machines) | `AzVM`             |
| [Lagringskonton](/azure/storage/common/storage-introduction)          | [Az.Storage](/powershell/module/az.storage/)                 | `AzStorageAccount` |
| [Key Vault](/azure/key-vault/key-vault-whatis)                          | [Az.KeyVault](/powershell/module/az.keyvault)                | `AzKeyVault`       |
| [Webbprogram](/azure/app-service)                                  | [Az.Websites](/powershell/module/az.websites)                | `AzWebApp`         |
| [SQL-databaser](/azure/sql-database)                                    | [Az.Sql](/powershell/module/az.sql)                          | `AzSqlDatabase`    |

En fullständig lista över moduler i Azure PowerShell finns i [listan med Azure PowerShell-moduler](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) på GitHub.

## <a name="telemetry"></a>Telemetri

Azure PowerShell samlar automatiskt in telemetridata som standard. Microsoft samlar in data för att upptäcka användningsmönster, identifiera vanliga problem och förbättra upplevelsen av Azure PowerShell. Microsoft Azure PowerShell samlar inte in privata eller personliga data. Om du vill inaktivera datainsamling måste du uttryckligen välja att göra det genom att köra [Disable-AzDataCollection](/powershell/module/az.accounts/disable-azdatacollection).

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a>Lär dig grunderna i Azure PowerShell med snabbstarter och självstudier

För att komma igång med Azure PowerShell kan du prova detaljerade självstudier där du konfigurerar virtuella datorer och lär dig att skicka frågor till dem.

> [!div class="nextstepaction"]
> [Skapa virtuella datorer med Azure PowerShell](azureps-vm-tutorial.yml)

Det finns även Azure PowerShell-snabbstarter för andra populära Azure-tjänster:

* [Skapa ett lagringskonto](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [Överföra objekt till och från Azure Blob Storage](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [Skapa och hämta hemligheter från Azure Key Vault](/azure/key-vault/quick-create-powershell)
* [Skapa en Azure SQL-databas och -brandvägg](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [Köra en container i Azure Container Instances](/azure/container-instances/container-instances-quickstart-powershell)
* [Skapa en VM-skalningsuppsättning](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [Skapa en standardlastbalanserare](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a>Nästa steg

* [Logga in med Azure PowerShell](authenticate-azureps.md)
* [Hantera Azure-prenumerationer med Azure PowerShell](manage-subscriptions-azureps.md)
* [Skapa huvudnamn för tjänsten med Azure PowerShell](create-azure-service-principal-azureps.md)
* Få hjälp från communityn:
  * [Azure-forumet på MSDN](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [Stack Overflow](https://go.microsoft.com/fwlink/?LinkId=320213)
