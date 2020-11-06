---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
ms.openlocfilehash: 35f9342fa66b46cfd029d6440d8d82134a6822a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573973"
---
# <span data-ttu-id="4f580-101">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="4f580-101">Get-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="4f580-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f580-102">SYNOPSIS</span></span>
<span data-ttu-id="4f580-103">Hämtar information om namn området för en händelse hubb eller hämtar en lista över alla namn rymder för händelser i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4f580-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f580-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f580-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f580-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f580-105">DESCRIPTION</span></span>
<span data-ttu-id="4f580-106">Get-AzureRmEventHubNamespace-cmdleten får antingen information om ett angivet namn område för händelse nav, eller en lista över alla namn områden i det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4f580-106">The Get-AzureRmEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="4f580-107">Om namn områdes namnet är angivet returneras informationen om ett namn område med en enskild händelse.</span><span class="sxs-lookup"><span data-stu-id="4f580-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="4f580-108">Om namn områdes namnet inte anges returneras en lista med namn områden.</span><span class="sxs-lookup"><span data-stu-id="4f580-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="4f580-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f580-109">EXAMPLES</span></span>

### <span data-ttu-id="4f580-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4f580-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="4f580-111">Hämtar information om namn områdes \` MyNamespaceName \` i MyResourceGroupName för resurs gruppen \` \` .</span><span class="sxs-lookup"><span data-stu-id="4f580-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="4f580-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f580-112">PARAMETERS</span></span>

### <span data-ttu-id="4f580-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f580-113">-DefaultProfile</span></span>
<span data-ttu-id="4f580-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f580-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f580-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="4f580-115">-Name</span></span>
<span data-ttu-id="4f580-116">Namn område för EventHub</span><span class="sxs-lookup"><span data-stu-id="4f580-116">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="4f580-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f580-117">-ResourceGroupName</span></span>
<span data-ttu-id="4f580-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="4f580-118">Resource Group Name</span></span>

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

### <span data-ttu-id="4f580-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f580-119">CommonParameters</span></span>
<span data-ttu-id="4f580-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f580-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f580-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f580-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f580-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f580-122">INPUTS</span></span>

### <span data-ttu-id="4f580-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4f580-123">System.String</span></span>

## <span data-ttu-id="4f580-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f580-124">OUTPUTS</span></span>

### <span data-ttu-id="4f580-125">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="4f580-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="4f580-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f580-126">NOTES</span></span>

## <span data-ttu-id="4f580-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f580-127">RELATED LINKS</span></span>
