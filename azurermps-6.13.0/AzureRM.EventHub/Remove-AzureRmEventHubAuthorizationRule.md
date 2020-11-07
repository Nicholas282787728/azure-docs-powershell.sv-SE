---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 35e3889603dc7e86a7d10679864adfd34a880b66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755845"
---
# <span data-ttu-id="fa8a3-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fa8a3-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="fa8a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa8a3-102">SYNOPSIS</span></span>
<span data-ttu-id="fa8a3-103">Tar bort den angivna auktoriseringsregeln för Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="fa8a3-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa8a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa8a3-104">SYNTAX</span></span>

### <span data-ttu-id="fa8a3-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fa8a3-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa8a3-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fa8a3-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-EventHub] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa8a3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa8a3-107">DESCRIPTION</span></span>
<span data-ttu-id="fa8a3-108">Remove-AzureRmEventHubAuthorizationRule-cmdleten tar bort och tar bort den angivna auktoriseringsregeln från den angivna händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="fa8a3-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="fa8a3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa8a3-109">EXAMPLES</span></span>

### <span data-ttu-id="fa8a3-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fa8a3-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="fa8a3-111">Tar bort \` MyAuthRuleName \` från namn områdes \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="fa8a3-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="fa8a3-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="fa8a3-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="fa8a3-113">Tar bort \` MyAuthRuleName från händelsehubben \` \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="fa8a3-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="fa8a3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa8a3-114">PARAMETERS</span></span>

### <span data-ttu-id="fa8a3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa8a3-115">-DefaultProfile</span></span>
<span data-ttu-id="fa8a3-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fa8a3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa8a3-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="fa8a3-117">-EventHub</span></span>
<span data-ttu-id="fa8a3-118">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="fa8a3-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa8a3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="fa8a3-119">-Force</span></span>
<span data-ttu-id="fa8a3-120">Fråga inte efter bekräftelse</span><span class="sxs-lookup"><span data-stu-id="fa8a3-120">Do not ask for confirmation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa8a3-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="fa8a3-121">-Name</span></span>
<span data-ttu-id="fa8a3-122">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="fa8a3-122">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa8a3-123">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="fa8a3-123">-Namespace</span></span>
<span data-ttu-id="fa8a3-124">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="fa8a3-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa8a3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa8a3-125">-PassThru</span></span>
<span data-ttu-id="fa8a3-126">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="fa8a3-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fa8a3-127">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="fa8a3-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa8a3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa8a3-128">-ResourceGroupName</span></span>
<span data-ttu-id="fa8a3-129">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="fa8a3-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa8a3-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fa8a3-130">-Confirm</span></span>
<span data-ttu-id="fa8a3-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fa8a3-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa8a3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa8a3-132">-WhatIf</span></span>
<span data-ttu-id="fa8a3-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fa8a3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa8a3-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fa8a3-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa8a3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa8a3-135">CommonParameters</span></span>
<span data-ttu-id="fa8a3-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa8a3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa8a3-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa8a3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa8a3-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa8a3-138">INPUTS</span></span>

### <span data-ttu-id="fa8a3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fa8a3-139">System.String</span></span>

## <span data-ttu-id="fa8a3-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa8a3-140">OUTPUTS</span></span>

### <span data-ttu-id="fa8a3-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa8a3-141">System.Boolean</span></span>

## <span data-ttu-id="fa8a3-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa8a3-142">NOTES</span></span>

## <span data-ttu-id="fa8a3-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa8a3-143">RELATED LINKS</span></span>
