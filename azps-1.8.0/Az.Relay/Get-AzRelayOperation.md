---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
ms.openlocfilehash: 166dbf5520531ec5a77fbc1e7017738d7201f664
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747237"
---
# <span data-ttu-id="6147c-101">Get-AzRelayOperation</span><span class="sxs-lookup"><span data-stu-id="6147c-101">Get-AzRelayOperation</span></span>

## <span data-ttu-id="6147c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6147c-102">SYNOPSIS</span></span>
<span data-ttu-id="6147c-103">Lista över relä åtgärder som stöds</span><span class="sxs-lookup"><span data-stu-id="6147c-103">List supported Relay Operations</span></span>

## <span data-ttu-id="6147c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6147c-104">SYNTAX</span></span>

```
Get-AzRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6147c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6147c-105">DESCRIPTION</span></span>
<span data-ttu-id="6147c-106">Cmdleten **Get-AzRelayOperation** visar vilka åtgärder som stöds av reläerna.</span><span class="sxs-lookup"><span data-stu-id="6147c-106">The **Get-AzRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="6147c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6147c-107">EXAMPLES</span></span>

### <span data-ttu-id="6147c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6147c-108">Example 1</span></span>
```
PS C:\> Get-AzRelayOperation

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

<span data-ttu-id="6147c-109">Visar åtgärder för återutsända relä</span><span class="sxs-lookup"><span data-stu-id="6147c-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="6147c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6147c-110">PARAMETERS</span></span>

### <span data-ttu-id="6147c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6147c-111">-DefaultProfile</span></span>
<span data-ttu-id="6147c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6147c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6147c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6147c-113">CommonParameters</span></span>
<span data-ttu-id="6147c-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6147c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6147c-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6147c-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6147c-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6147c-116">INPUTS</span></span>

### <span data-ttu-id="6147c-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="6147c-117">None</span></span>

## <span data-ttu-id="6147c-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6147c-118">OUTPUTS</span></span>

### <span data-ttu-id="6147c-119">Microsoft. Azure. commands. Relay. Models. PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="6147c-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="6147c-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6147c-120">NOTES</span></span>

## <span data-ttu-id="6147c-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6147c-121">RELATED LINKS</span></span>
