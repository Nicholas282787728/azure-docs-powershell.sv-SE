---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
ms.openlocfilehash: 7c0c09d69e76b082bfb7d300f7d67b001c1dd329
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922925"
---
# <span data-ttu-id="beb1f-101">Get-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="beb1f-101">Get-AzEventHubNamespace</span></span>

## <span data-ttu-id="beb1f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="beb1f-102">SYNOPSIS</span></span>
<span data-ttu-id="beb1f-103">Hämtar information om namn området för en händelse hubb eller hämtar en lista över alla namn rymder för händelser i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="beb1f-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

## <span data-ttu-id="beb1f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="beb1f-104">SYNTAX</span></span>

```
Get-AzEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="beb1f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="beb1f-105">DESCRIPTION</span></span>
<span data-ttu-id="beb1f-106">Get-AzEventHubNamespace-cmdleten får antingen information om ett angivet namn område för händelse nav, eller en lista över alla namn områden i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="beb1f-106">The Get-AzEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="beb1f-107">Om namn områdes namnet är angivet returneras informationen om ett namn område med en enskild händelse.</span><span class="sxs-lookup"><span data-stu-id="beb1f-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="beb1f-108">Om namn områdes namnet inte anges returneras en lista med namn områden.</span><span class="sxs-lookup"><span data-stu-id="beb1f-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="beb1f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="beb1f-109">EXAMPLES</span></span>

### <span data-ttu-id="beb1f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="beb1f-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="beb1f-111">Hämtar information om namn områdes \` MyNamespaceName \` i MyResourceGroupName för resurs gruppen \` \` .</span><span class="sxs-lookup"><span data-stu-id="beb1f-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="beb1f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="beb1f-112">PARAMETERS</span></span>

### <span data-ttu-id="beb1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beb1f-113">-DefaultProfile</span></span>
<span data-ttu-id="beb1f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="beb1f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="beb1f-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="beb1f-115">-Name</span></span>
<span data-ttu-id="beb1f-116">Namn område för EventHub</span><span class="sxs-lookup"><span data-stu-id="beb1f-116">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beb1f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beb1f-117">-ResourceGroupName</span></span>
<span data-ttu-id="beb1f-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="beb1f-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beb1f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beb1f-119">CommonParameters</span></span>
<span data-ttu-id="beb1f-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beb1f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beb1f-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beb1f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beb1f-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="beb1f-122">INPUTS</span></span>

### <span data-ttu-id="beb1f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="beb1f-123">System.String</span></span>

## <span data-ttu-id="beb1f-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="beb1f-124">OUTPUTS</span></span>

### <span data-ttu-id="beb1f-125">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="beb1f-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="beb1f-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="beb1f-126">NOTES</span></span>

## <span data-ttu-id="beb1f-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="beb1f-127">RELATED LINKS</span></span>
