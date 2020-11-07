---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 9d59a974a29743004228efb414a92627782bd8e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757035"
---
# <span data-ttu-id="4dcfe-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4dcfe-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="4dcfe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4dcfe-102">SYNOPSIS</span></span>
<span data-ttu-id="4dcfe-103">Tar bort en princip definition.</span><span class="sxs-lookup"><span data-stu-id="4dcfe-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dcfe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4dcfe-104">SYNTAX</span></span>

### <span data-ttu-id="4dcfe-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4dcfe-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dcfe-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dcfe-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dcfe-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dcfe-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dcfe-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dcfe-108">IdParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dcfe-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4dcfe-109">DESCRIPTION</span></span>
<span data-ttu-id="4dcfe-110">Cmdleten **Remove-AzureRmPolicyDefinition** tar bort en princip definition.</span><span class="sxs-lookup"><span data-stu-id="4dcfe-110">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="4dcfe-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4dcfe-111">EXAMPLES</span></span>

### <span data-ttu-id="4dcfe-112">Exempel 1: ta bort princip definitionen utifrån namn</span><span class="sxs-lookup"><span data-stu-id="4dcfe-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="4dcfe-113">Det här kommandot tar bort den angivna princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="4dcfe-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="4dcfe-114">Exempel 2: ta bort princip definitionen efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="4dcfe-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="4dcfe-115">Det första kommandot hämtar princip definitionen med namnet VMPolicyDefinition med hjälp av Get-AzureRmPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dcfe-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="4dcfe-116">Kommandot sparar det i $PolicyDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="4dcfe-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="4dcfe-117">Det andra kommandot tar bort princip definitionen som identifieras av egenskapen **ResourceID** för $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="4dcfe-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="4dcfe-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4dcfe-118">PARAMETERS</span></span>

### <span data-ttu-id="4dcfe-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4dcfe-119">-ApiVersion</span></span>
<span data-ttu-id="4dcfe-120">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4dcfe-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4dcfe-121">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="4dcfe-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4dcfe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dcfe-122">-DefaultProfile</span></span>
<span data-ttu-id="4dcfe-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4dcfe-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4dcfe-124">-Force</span><span class="sxs-lookup"><span data-stu-id="4dcfe-124">-Force</span></span>
<span data-ttu-id="4dcfe-125">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4dcfe-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4dcfe-126">-ID</span><span class="sxs-lookup"><span data-stu-id="4dcfe-126">-Id</span></span>
<span data-ttu-id="4dcfe-127">Anger det fullständiga resurs-ID för princip definitionen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="4dcfe-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4dcfe-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4dcfe-128">-InformationAction</span></span>
<span data-ttu-id="4dcfe-129">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="4dcfe-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="4dcfe-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4dcfe-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4dcfe-131">Vidare</span><span class="sxs-lookup"><span data-stu-id="4dcfe-131">Continue</span></span>
- <span data-ttu-id="4dcfe-132">Över</span><span class="sxs-lookup"><span data-stu-id="4dcfe-132">Ignore</span></span>
- <span data-ttu-id="4dcfe-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="4dcfe-133">Inquire</span></span>
- <span data-ttu-id="4dcfe-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4dcfe-134">SilentlyContinue</span></span>
- <span data-ttu-id="4dcfe-135">Stanna</span><span class="sxs-lookup"><span data-stu-id="4dcfe-135">Stop</span></span>
- <span data-ttu-id="4dcfe-136">Avbryt</span><span class="sxs-lookup"><span data-stu-id="4dcfe-136">Suspend</span></span>

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

### <span data-ttu-id="4dcfe-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4dcfe-137">-InformationVariable</span></span>
<span data-ttu-id="4dcfe-138">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="4dcfe-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4dcfe-139">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="4dcfe-139">-ManagementGroupName</span></span>
<span data-ttu-id="4dcfe-140">Namnet på hanterings gruppen för princip definitionen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4dcfe-140">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="4dcfe-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="4dcfe-141">-Name</span></span>
<span data-ttu-id="4dcfe-142">Anger namnet på princip definitionen som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="4dcfe-142">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4dcfe-143">-För</span><span class="sxs-lookup"><span data-stu-id="4dcfe-143">-Pre</span></span>
<span data-ttu-id="4dcfe-144">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4dcfe-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4dcfe-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4dcfe-145">-SubscriptionId</span></span>
<span data-ttu-id="4dcfe-146">Abonnemangs-ID för princip definitionen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4dcfe-146">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="4dcfe-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4dcfe-147">-Confirm</span></span>
<span data-ttu-id="4dcfe-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4dcfe-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dcfe-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dcfe-149">-WhatIf</span></span>
<span data-ttu-id="4dcfe-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4dcfe-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dcfe-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4dcfe-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dcfe-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dcfe-152">CommonParameters</span></span>
<span data-ttu-id="4dcfe-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dcfe-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dcfe-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dcfe-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dcfe-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4dcfe-155">INPUTS</span></span>

## <span data-ttu-id="4dcfe-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4dcfe-156">OUTPUTS</span></span>

## <span data-ttu-id="4dcfe-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4dcfe-157">NOTES</span></span>

## <span data-ttu-id="4dcfe-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4dcfe-158">RELATED LINKS</span></span>

[<span data-ttu-id="4dcfe-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4dcfe-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="4dcfe-160">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4dcfe-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="4dcfe-161">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4dcfe-161">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


