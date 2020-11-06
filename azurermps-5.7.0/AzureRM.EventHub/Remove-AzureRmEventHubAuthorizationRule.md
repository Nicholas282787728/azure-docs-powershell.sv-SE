---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: c15528befc90a0249101602fef9b178e7a63c0ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577234"
---
# <span data-ttu-id="a909c-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a909c-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="a909c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a909c-102">SYNOPSIS</span></span>
<span data-ttu-id="a909c-103">Tar bort den angivna auktoriseringsregeln för Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="a909c-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a909c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a909c-104">SYNTAX</span></span>

### <span data-ttu-id="a909c-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a909c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a909c-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a909c-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-EventHub] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a909c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a909c-107">DESCRIPTION</span></span>
<span data-ttu-id="a909c-108">Remove-AzureRmEventHubAuthorizationRule-cmdleten tar bort och tar bort den angivna auktoriseringsregeln från den angivna händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="a909c-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="a909c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a909c-109">EXAMPLES</span></span>

### <span data-ttu-id="a909c-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a909c-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

### <span data-ttu-id="a909c-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a909c-111">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="a909c-112">Tar bort \` MyAuthRuleName från händelsehubben \` \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="a909c-112">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="a909c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a909c-113">PARAMETERS</span></span>

### <span data-ttu-id="a909c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a909c-114">-DefaultProfile</span></span>
<span data-ttu-id="a909c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a909c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a909c-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="a909c-116">-EventHub</span></span>
<span data-ttu-id="a909c-117">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="a909c-117">EventHub Name</span></span>

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

### <span data-ttu-id="a909c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a909c-118">-Force</span></span>
<span data-ttu-id="a909c-119">Fråga inte efter bekräftelse</span><span class="sxs-lookup"><span data-stu-id="a909c-119">Do not ask for confirmation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a909c-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="a909c-120">-Name</span></span>
<span data-ttu-id="a909c-121">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="a909c-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="a909c-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="a909c-122">-Namespace</span></span>
<span data-ttu-id="a909c-123">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="a909c-123">Namespace Name</span></span>

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

### <span data-ttu-id="a909c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a909c-124">-PassThru</span></span>
<span data-ttu-id="a909c-125">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="a909c-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a909c-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="a909c-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a909c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a909c-127">-ResourceGroupName</span></span>
<span data-ttu-id="a909c-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a909c-128">Resource Group Name</span></span>

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

### <span data-ttu-id="a909c-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a909c-129">-Confirm</span></span>
<span data-ttu-id="a909c-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a909c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a909c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a909c-131">-WhatIf</span></span>
<span data-ttu-id="a909c-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a909c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a909c-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a909c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a909c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a909c-134">CommonParameters</span></span>
<span data-ttu-id="a909c-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a909c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a909c-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a909c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a909c-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a909c-137">INPUTS</span></span>

### <span data-ttu-id="a909c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a909c-138">System.String</span></span>


## <span data-ttu-id="a909c-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a909c-139">OUTPUTS</span></span>

### <span data-ttu-id="a909c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a909c-140">System.Boolean</span></span>


## <span data-ttu-id="a909c-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a909c-141">NOTES</span></span>

## <span data-ttu-id="a909c-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a909c-142">RELATED LINKS</span></span>
