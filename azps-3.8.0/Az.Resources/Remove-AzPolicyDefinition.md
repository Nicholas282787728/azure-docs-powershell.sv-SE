---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: bd374f19a282ccafc3201a2965c33d4e8a3007ab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089486"
---
# <span data-ttu-id="f4dad-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4dad-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="f4dad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4dad-102">SYNOPSIS</span></span>
<span data-ttu-id="f4dad-103">Tar bort en princip definition.</span><span class="sxs-lookup"><span data-stu-id="f4dad-103">Removes a policy definition.</span></span>

## <span data-ttu-id="f4dad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4dad-104">SYNTAX</span></span>

### <span data-ttu-id="f4dad-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f4dad-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4dad-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4dad-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4dad-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4dad-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4dad-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4dad-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4dad-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4dad-109">DESCRIPTION</span></span>
<span data-ttu-id="f4dad-110">Cmdleten **Remove-AzPolicyDefinition** tar bort en princip definition.</span><span class="sxs-lookup"><span data-stu-id="f4dad-110">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="f4dad-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4dad-111">EXAMPLES</span></span>

### <span data-ttu-id="f4dad-112">Exempel 1: ta bort princip definitionen utifrån namn</span><span class="sxs-lookup"><span data-stu-id="f4dad-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="f4dad-113">Det här kommandot tar bort den angivna princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="f4dad-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="f4dad-114">Exempel 2: ta bort princip definitionen efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="f4dad-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="f4dad-115">Det första kommandot hämtar princip definitionen med namnet VMPolicyDefinition med hjälp av Get-AzPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4dad-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="f4dad-116">Kommandot sparar det i $PolicyDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="f4dad-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="f4dad-117">Det andra kommandot tar bort princip definitionen som identifieras av egenskapen **ResourceID** för $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="f4dad-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="f4dad-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4dad-118">PARAMETERS</span></span>

### <span data-ttu-id="f4dad-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f4dad-119">-ApiVersion</span></span>
<span data-ttu-id="f4dad-120">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f4dad-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f4dad-121">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="f4dad-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4dad-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4dad-122">-DefaultProfile</span></span>
<span data-ttu-id="f4dad-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f4dad-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4dad-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f4dad-124">-Force</span></span>
<span data-ttu-id="f4dad-125">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f4dad-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f4dad-126">-ID</span><span class="sxs-lookup"><span data-stu-id="f4dad-126">-Id</span></span>
<span data-ttu-id="f4dad-127">Anger det fullständiga resurs-ID för princip definitionen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="f4dad-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4dad-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="f4dad-128">-ManagementGroupName</span></span>
<span data-ttu-id="f4dad-129">Namnet på hanterings gruppen för princip definitionen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f4dad-129">The name of the management group of the policy definition to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4dad-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="f4dad-130">-Name</span></span>
<span data-ttu-id="f4dad-131">Anger namnet på princip definitionen som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="f4dad-131">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4dad-132">-För</span><span class="sxs-lookup"><span data-stu-id="f4dad-132">-Pre</span></span>
<span data-ttu-id="f4dad-133">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f4dad-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f4dad-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4dad-134">-SubscriptionId</span></span>
<span data-ttu-id="f4dad-135">Abonnemangs-ID för princip definitionen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f4dad-135">The subscription ID of the policy definition to delete.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4dad-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f4dad-136">-Confirm</span></span>
<span data-ttu-id="f4dad-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f4dad-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4dad-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4dad-138">-WhatIf</span></span>
<span data-ttu-id="f4dad-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f4dad-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4dad-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f4dad-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4dad-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4dad-141">CommonParameters</span></span>
<span data-ttu-id="f4dad-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4dad-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4dad-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4dad-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4dad-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4dad-144">INPUTS</span></span>

### <span data-ttu-id="f4dad-145">System. String</span><span class="sxs-lookup"><span data-stu-id="f4dad-145">System.String</span></span>

### <span data-ttu-id="f4dad-146">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f4dad-146">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f4dad-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4dad-147">OUTPUTS</span></span>

### <span data-ttu-id="f4dad-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4dad-148">System.Boolean</span></span>

## <span data-ttu-id="f4dad-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4dad-149">NOTES</span></span>

## <span data-ttu-id="f4dad-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4dad-150">RELATED LINKS</span></span>

[<span data-ttu-id="f4dad-151">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4dad-151">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="f4dad-152">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4dad-152">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="f4dad-153">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4dad-153">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


