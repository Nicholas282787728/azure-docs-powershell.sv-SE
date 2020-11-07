---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 9e7cfbe1ec0810b9d18f884306535d37a6110dd2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754061"
---
# <span data-ttu-id="20078-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="20078-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="20078-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20078-102">SYNOPSIS</span></span>
<span data-ttu-id="20078-103">Tar bort den angivna auktoriseringsregeln för Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="20078-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="20078-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20078-104">SYNTAX</span></span>

### <span data-ttu-id="20078-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="20078-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20078-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="20078-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20078-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20078-107">DESCRIPTION</span></span>
<span data-ttu-id="20078-108">Remove-AzEventHubAuthorizationRule-cmdleten tar bort och tar bort den angivna auktoriseringsregeln från den angivna händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="20078-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="20078-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20078-109">EXAMPLES</span></span>

### <span data-ttu-id="20078-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="20078-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="20078-111">Tar bort \` MyAuthRuleName \` från namn områdes \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="20078-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="20078-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="20078-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="20078-113">Tar bort \` MyAuthRuleName från händelsehubben \` \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="20078-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="20078-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20078-114">PARAMETERS</span></span>

### <span data-ttu-id="20078-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20078-115">-DefaultProfile</span></span>
<span data-ttu-id="20078-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20078-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20078-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="20078-117">-EventHub</span></span>
<span data-ttu-id="20078-118">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="20078-118">EventHub Name</span></span>

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

### <span data-ttu-id="20078-119">-Force</span><span class="sxs-lookup"><span data-stu-id="20078-119">-Force</span></span>
<span data-ttu-id="20078-120">Fråga inte efter bekräftelse</span><span class="sxs-lookup"><span data-stu-id="20078-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="20078-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="20078-121">-Name</span></span>
<span data-ttu-id="20078-122">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="20078-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="20078-123">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="20078-123">-Namespace</span></span>
<span data-ttu-id="20078-124">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="20078-124">Namespace Name</span></span>

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

### <span data-ttu-id="20078-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20078-125">-PassThru</span></span>
<span data-ttu-id="20078-126">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="20078-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="20078-127">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="20078-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="20078-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20078-128">-ResourceGroupName</span></span>
<span data-ttu-id="20078-129">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="20078-129">Resource Group Name</span></span>

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

### <span data-ttu-id="20078-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="20078-130">-Confirm</span></span>
<span data-ttu-id="20078-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="20078-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20078-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20078-132">-WhatIf</span></span>
<span data-ttu-id="20078-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="20078-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20078-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="20078-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20078-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20078-135">CommonParameters</span></span>
<span data-ttu-id="20078-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20078-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20078-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20078-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20078-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20078-138">INPUTS</span></span>

### <span data-ttu-id="20078-139">System. String</span><span class="sxs-lookup"><span data-stu-id="20078-139">System.String</span></span>

## <span data-ttu-id="20078-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20078-140">OUTPUTS</span></span>

### <span data-ttu-id="20078-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="20078-141">System.Boolean</span></span>

## <span data-ttu-id="20078-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20078-142">NOTES</span></span>

## <span data-ttu-id="20078-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20078-143">RELATED LINKS</span></span>
