---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
ms.openlocfilehash: 8be39cb4b4b173d3b87efbf0b7ecea72ae233061
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756286"
---
# <span data-ttu-id="cfeae-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="cfeae-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="cfeae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cfeae-102">SYNOPSIS</span></span>
<span data-ttu-id="cfeae-103">Skapar en ny primär eller sekundär nycklar för den angivna auktoriseringsregeln för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="cfeae-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfeae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cfeae-104">SYNTAX</span></span>

### <span data-ttu-id="cfeae-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cfeae-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfeae-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="cfeae-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-RegenerateKey] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cfeae-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cfeae-107">DESCRIPTION</span></span>
<span data-ttu-id="cfeae-108">New-AzureRmEventHubKey cmdlet återskapar den primära eller sekundära säkerhets associationen för den angivna auktoriseringsregeln för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="cfeae-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="cfeae-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cfeae-109">EXAMPLES</span></span>

### <span data-ttu-id="cfeae-110">Exempel 1,1</span><span class="sxs-lookup"><span data-stu-id="cfeae-110">Example 1.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="cfeae-111">Återskapar primär nyckeln för auktoriseringsregeln \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="cfeae-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="cfeae-112">Exempel 1,2</span><span class="sxs-lookup"><span data-stu-id="cfeae-112">Example 1.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="cfeae-113">Återskapar primär nyckeln för auktoriseringsregeln \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="cfeae-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="cfeae-114">Exempel 2,1</span><span class="sxs-lookup"><span data-stu-id="cfeae-114">Example 2.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="cfeae-115">Exempel 2,2</span><span class="sxs-lookup"><span data-stu-id="cfeae-115">Example 2.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="cfeae-116">Återskapar den sekundära nyckeln för \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="cfeae-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="cfeae-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cfeae-117">PARAMETERS</span></span>

### <span data-ttu-id="cfeae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfeae-118">-DefaultProfile</span></span>
<span data-ttu-id="cfeae-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cfeae-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfeae-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="cfeae-120">-EventHub</span></span>
<span data-ttu-id="cfeae-121">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="cfeae-121">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfeae-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="cfeae-122">-Name</span></span>
<span data-ttu-id="cfeae-123">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="cfeae-123">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfeae-124">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="cfeae-124">-Namespace</span></span>
<span data-ttu-id="cfeae-125">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="cfeae-125">Namespace Name</span></span>

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

### <span data-ttu-id="cfeae-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="cfeae-126">-RegenerateKey</span></span>
<span data-ttu-id="cfeae-127">Återskapa nycklar – "PrimaryKey"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="cfeae-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfeae-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfeae-128">-ResourceGroupName</span></span>
<span data-ttu-id="cfeae-129">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="cfeae-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfeae-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cfeae-130">-Confirm</span></span>
<span data-ttu-id="cfeae-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cfeae-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfeae-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfeae-132">-WhatIf</span></span>
<span data-ttu-id="cfeae-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cfeae-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfeae-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cfeae-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfeae-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfeae-135">CommonParameters</span></span>
<span data-ttu-id="cfeae-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfeae-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cfeae-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfeae-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfeae-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cfeae-138">INPUTS</span></span>

### <span data-ttu-id="cfeae-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cfeae-139">System.String</span></span>


## <span data-ttu-id="cfeae-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cfeae-140">OUTPUTS</span></span>

### <span data-ttu-id="cfeae-141">Microsoft. Azure. commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="cfeae-141">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="cfeae-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cfeae-142">NOTES</span></span>

## <span data-ttu-id="cfeae-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cfeae-143">RELATED LINKS</span></span>
