---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayOperation.md
ms.openlocfilehash: e7f45be6a39cdd2b7f2d11736d2a5f62831244c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576124"
---
# <span data-ttu-id="48c33-101">Get-AzureRmRelayOperation</span><span class="sxs-lookup"><span data-stu-id="48c33-101">Get-AzureRmRelayOperation</span></span>

## <span data-ttu-id="48c33-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48c33-102">SYNOPSIS</span></span>
<span data-ttu-id="48c33-103">Lista över relä åtgärder som stöds</span><span class="sxs-lookup"><span data-stu-id="48c33-103">List supported Relay Operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48c33-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48c33-104">SYNTAX</span></span>

```
Get-AzureRmRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48c33-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48c33-105">DESCRIPTION</span></span>
<span data-ttu-id="48c33-106">Cmdleten **Get-AzureRmRelayOperation** visar vilka åtgärder som stöds av reläerna.</span><span class="sxs-lookup"><span data-stu-id="48c33-106">The **Get-AzureRmRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="48c33-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48c33-107">EXAMPLES</span></span>

### <span data-ttu-id="48c33-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="48c33-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRelayOperation

Name                                                                            Display
----                                                                            -------
Microsoft.Relay/checkNamespaceAvailability/action                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/register/action                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/write                                                Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/read                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/Delete                                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/write                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/delete                            Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/listkeys/action                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/write                              Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/read                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/Delete                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/write           Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/delete          Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/write                                      Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/read                                       Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/Delete                                     Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/write                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/delete                  Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/listkeys/action         Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
```

<span data-ttu-id="48c33-109">Visar åtgärder för återutsända relä</span><span class="sxs-lookup"><span data-stu-id="48c33-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="48c33-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48c33-110">PARAMETERS</span></span>

### <span data-ttu-id="48c33-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48c33-111">-DefaultProfile</span></span>
<span data-ttu-id="48c33-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="48c33-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c33-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48c33-113">CommonParameters</span></span>
<span data-ttu-id="48c33-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48c33-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="48c33-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48c33-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48c33-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48c33-116">INPUTS</span></span>

### <span data-ttu-id="48c33-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="48c33-117">None</span></span>


## <span data-ttu-id="48c33-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48c33-118">OUTPUTS</span></span>

### <span data-ttu-id="48c33-119">Microsoft. Azure. commands. Relay. Models. PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="48c33-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span></span>


## <span data-ttu-id="48c33-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48c33-120">NOTES</span></span>

## <span data-ttu-id="48c33-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48c33-121">RELATED LINKS</span></span>
