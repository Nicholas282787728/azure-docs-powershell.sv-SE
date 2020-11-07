---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: f932e566d9fe6639e19e4f906775282cd17315d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920049"
---
# <span data-ttu-id="2c1b1-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2c1b1-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="2c1b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c1b1-102">SYNOPSIS</span></span>
<span data-ttu-id="2c1b1-103">Tar bort en princip definition.</span><span class="sxs-lookup"><span data-stu-id="2c1b1-103">Removes a policy definition.</span></span>

## <span data-ttu-id="2c1b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c1b1-104">SYNTAX</span></span>

### <span data-ttu-id="2c1b1-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2c1b1-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c1b1-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c1b1-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c1b1-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c1b1-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c1b1-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c1b1-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c1b1-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c1b1-109">DESCRIPTION</span></span>
<span data-ttu-id="2c1b1-110">Cmdleten **Remove-AzPolicyDefinition** tar bort en princip definition.</span><span class="sxs-lookup"><span data-stu-id="2c1b1-110">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="2c1b1-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c1b1-111">EXAMPLES</span></span>

### <span data-ttu-id="2c1b1-112">Exempel 1: ta bort princip definitionen utifrån namn</span><span class="sxs-lookup"><span data-stu-id="2c1b1-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="2c1b1-113">Det här kommandot tar bort den angivna princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="2c1b1-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="2c1b1-114">Exempel 2: ta bort princip definitionen efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="2c1b1-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="2c1b1-115">Det första kommandot hämtar princip definitionen med namnet VMPolicyDefinition med hjälp av Get-AzPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c1b1-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="2c1b1-116">Kommandot sparar det i $PolicyDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="2c1b1-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="2c1b1-117">Det andra kommandot tar bort princip definitionen som identifieras av egenskapen **ResourceID** för $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="2c1b1-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="2c1b1-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c1b1-118">PARAMETERS</span></span>

### <span data-ttu-id="2c1b1-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2c1b1-119">-ApiVersion</span></span>
<span data-ttu-id="2c1b1-120">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="2c1b1-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2c1b1-121">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="2c1b1-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="2c1b1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c1b1-122">-DefaultProfile</span></span>
<span data-ttu-id="2c1b1-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2c1b1-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c1b1-124">-Force</span><span class="sxs-lookup"><span data-stu-id="2c1b1-124">-Force</span></span>
<span data-ttu-id="2c1b1-125">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2c1b1-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2c1b1-126">-ID</span><span class="sxs-lookup"><span data-stu-id="2c1b1-126">-Id</span></span>
<span data-ttu-id="2c1b1-127">Anger det fullständiga resurs-ID för princip definitionen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="2c1b1-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2c1b1-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="2c1b1-128">-ManagementGroupName</span></span>
<span data-ttu-id="2c1b1-129">Namnet på hanterings gruppen för princip definitionen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="2c1b1-129">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="2c1b1-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="2c1b1-130">-Name</span></span>
<span data-ttu-id="2c1b1-131">Anger namnet på princip definitionen som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="2c1b1-131">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2c1b1-132">-För</span><span class="sxs-lookup"><span data-stu-id="2c1b1-132">-Pre</span></span>
<span data-ttu-id="2c1b1-133">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="2c1b1-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2c1b1-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c1b1-134">-SubscriptionId</span></span>
<span data-ttu-id="2c1b1-135">Abonnemangs-ID för princip definitionen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="2c1b1-135">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="2c1b1-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2c1b1-136">-Confirm</span></span>
<span data-ttu-id="2c1b1-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2c1b1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c1b1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c1b1-138">-WhatIf</span></span>
<span data-ttu-id="2c1b1-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2c1b1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c1b1-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2c1b1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c1b1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c1b1-141">CommonParameters</span></span>
<span data-ttu-id="2c1b1-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c1b1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c1b1-143">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c1b1-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c1b1-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c1b1-144">INPUTS</span></span>

### <span data-ttu-id="2c1b1-145">System. String</span><span class="sxs-lookup"><span data-stu-id="2c1b1-145">System.String</span></span>

### <span data-ttu-id="2c1b1-146">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2c1b1-146">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2c1b1-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c1b1-147">OUTPUTS</span></span>

### <span data-ttu-id="2c1b1-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c1b1-148">System.Boolean</span></span>

## <span data-ttu-id="2c1b1-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c1b1-149">NOTES</span></span>

## <span data-ttu-id="2c1b1-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c1b1-150">RELATED LINKS</span></span>

[<span data-ttu-id="2c1b1-151">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2c1b1-151">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="2c1b1-152">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2c1b1-152">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="2c1b1-153">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2c1b1-153">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


