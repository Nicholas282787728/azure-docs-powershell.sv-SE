---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
ms.openlocfilehash: cec41bda56da33f22def6c44752effb3d705b935
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755876"
---
# <span data-ttu-id="003af-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="003af-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="003af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="003af-102">SYNOPSIS</span></span>
<span data-ttu-id="003af-103">Tar bort det angivna namn området för Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="003af-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="003af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="003af-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="003af-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="003af-105">DESCRIPTION</span></span>
<span data-ttu-id="003af-106">Remove-AzureRmEventHubNamespace-cmdleten tar bort och tar bort det angivna namn området för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="003af-106">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="003af-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="003af-107">EXAMPLES</span></span>

### <span data-ttu-id="003af-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="003af-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="003af-109">Tar bort namn områdes \` MyNamespaceName \` för Event Hub i resurs gruppen \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="003af-109">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="003af-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="003af-110">PARAMETERS</span></span>

### <span data-ttu-id="003af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="003af-111">-DefaultProfile</span></span>
<span data-ttu-id="003af-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="003af-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="003af-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="003af-113">-Name</span></span>
<span data-ttu-id="003af-114">Namn område för EventHub</span><span class="sxs-lookup"><span data-stu-id="003af-114">EventHub Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003af-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="003af-115">-ResourceGroupName</span></span>
<span data-ttu-id="003af-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="003af-116">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003af-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="003af-117">-Confirm</span></span>
<span data-ttu-id="003af-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="003af-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="003af-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="003af-119">-WhatIf</span></span>
<span data-ttu-id="003af-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="003af-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="003af-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="003af-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="003af-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="003af-122">CommonParameters</span></span>
<span data-ttu-id="003af-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="003af-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="003af-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="003af-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="003af-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="003af-125">INPUTS</span></span>

### <span data-ttu-id="003af-126">System. String</span><span class="sxs-lookup"><span data-stu-id="003af-126">System.String</span></span>


## <span data-ttu-id="003af-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="003af-127">OUTPUTS</span></span>

### <span data-ttu-id="003af-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="003af-128">System.Object</span></span>

## <span data-ttu-id="003af-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="003af-129">NOTES</span></span>

## <span data-ttu-id="003af-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="003af-130">RELATED LINKS</span></span>
