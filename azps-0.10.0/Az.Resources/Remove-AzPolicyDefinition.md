---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: 8cd1ee1d8f32bd203e9fb2d8ac5d75c2d6b2938d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923825"
---
# <span data-ttu-id="a015b-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a015b-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="a015b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a015b-102">SYNOPSIS</span></span>
<span data-ttu-id="a015b-103">Tar bort en princip definition.</span><span class="sxs-lookup"><span data-stu-id="a015b-103">Removes a policy definition.</span></span>

## <span data-ttu-id="a015b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a015b-104">SYNTAX</span></span>

### <span data-ttu-id="a015b-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a015b-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a015b-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a015b-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a015b-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a015b-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a015b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a015b-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a015b-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a015b-109">DESCRIPTION</span></span>
<span data-ttu-id="a015b-110">Cmdleten **Remove-AzPolicyDefinition** tar bort en princip definition.</span><span class="sxs-lookup"><span data-stu-id="a015b-110">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="a015b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a015b-111">EXAMPLES</span></span>

### <span data-ttu-id="a015b-112">Exempel 1: ta bort princip definitionen utifrån namn</span><span class="sxs-lookup"><span data-stu-id="a015b-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="a015b-113">Det här kommandot tar bort den angivna princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="a015b-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="a015b-114">Exempel 2: ta bort princip definitionen efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="a015b-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="a015b-115">Det första kommandot hämtar princip definitionen med namnet VMPolicyDefinition med hjälp av Get-AzPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a015b-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="a015b-116">Kommandot sparar det i $PolicyDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="a015b-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="a015b-117">Det andra kommandot tar bort princip definitionen som identifieras av egenskapen **ResourceID** för $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="a015b-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="a015b-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a015b-118">PARAMETERS</span></span>

### <span data-ttu-id="a015b-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a015b-119">-ApiVersion</span></span>
<span data-ttu-id="a015b-120">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a015b-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a015b-121">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="a015b-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a015b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a015b-122">-DefaultProfile</span></span>
<span data-ttu-id="a015b-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a015b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a015b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a015b-124">-Force</span></span>
<span data-ttu-id="a015b-125">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a015b-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a015b-126">-ID</span><span class="sxs-lookup"><span data-stu-id="a015b-126">-Id</span></span>
<span data-ttu-id="a015b-127">Anger det fullständiga resurs-ID för princip definitionen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="a015b-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a015b-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a015b-128">-InformationAction</span></span>
<span data-ttu-id="a015b-129">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="a015b-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="a015b-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a015b-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a015b-131">Vidare</span><span class="sxs-lookup"><span data-stu-id="a015b-131">Continue</span></span>
- <span data-ttu-id="a015b-132">Över</span><span class="sxs-lookup"><span data-stu-id="a015b-132">Ignore</span></span>
- <span data-ttu-id="a015b-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="a015b-133">Inquire</span></span>
- <span data-ttu-id="a015b-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a015b-134">SilentlyContinue</span></span>
- <span data-ttu-id="a015b-135">Stanna</span><span class="sxs-lookup"><span data-stu-id="a015b-135">Stop</span></span>
- <span data-ttu-id="a015b-136">Avbryt</span><span class="sxs-lookup"><span data-stu-id="a015b-136">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a015b-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a015b-137">-InformationVariable</span></span>
<span data-ttu-id="a015b-138">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="a015b-138">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a015b-139">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a015b-139">-ManagementGroupName</span></span>
<span data-ttu-id="a015b-140">Namnet på hanterings gruppen för princip definitionen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="a015b-140">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="a015b-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="a015b-141">-Name</span></span>
<span data-ttu-id="a015b-142">Anger namnet på princip definitionen som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="a015b-142">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a015b-143">-För</span><span class="sxs-lookup"><span data-stu-id="a015b-143">-Pre</span></span>
<span data-ttu-id="a015b-144">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a015b-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a015b-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a015b-145">-SubscriptionId</span></span>
<span data-ttu-id="a015b-146">Abonnemangs-ID för princip definitionen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="a015b-146">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="a015b-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a015b-147">-Confirm</span></span>
<span data-ttu-id="a015b-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a015b-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a015b-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a015b-149">-WhatIf</span></span>
<span data-ttu-id="a015b-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a015b-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a015b-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a015b-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a015b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a015b-152">CommonParameters</span></span>
<span data-ttu-id="a015b-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a015b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a015b-154">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a015b-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a015b-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a015b-155">INPUTS</span></span>

## <span data-ttu-id="a015b-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a015b-156">OUTPUTS</span></span>

## <span data-ttu-id="a015b-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a015b-157">NOTES</span></span>

## <span data-ttu-id="a015b-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a015b-158">RELATED LINKS</span></span>

[<span data-ttu-id="a015b-159">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a015b-159">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="a015b-160">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a015b-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="a015b-161">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a015b-161">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


