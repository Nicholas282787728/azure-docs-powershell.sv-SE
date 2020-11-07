---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicydefinition
schema: 2.0.0
ms.openlocfilehash: 03da83268a06ac4026604728281b10f767fab9a3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931122"
---
# <span data-ttu-id="b5040-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b5040-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="b5040-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5040-102">SYNOPSIS</span></span>
<span data-ttu-id="b5040-103">Tar bort en princip definition.</span><span class="sxs-lookup"><span data-stu-id="b5040-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5040-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5040-104">SYNTAX</span></span>

### <span data-ttu-id="b5040-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b5040-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5040-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5040-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5040-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5040-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5040-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5040-108">IdParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5040-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5040-109">DESCRIPTION</span></span>
<span data-ttu-id="b5040-110">Cmdleten **Remove-AzureRmPolicyDefinition** tar bort en princip definition.</span><span class="sxs-lookup"><span data-stu-id="b5040-110">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="b5040-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5040-111">EXAMPLES</span></span>

### <span data-ttu-id="b5040-112">Exempel 1: ta bort princip definitionen utifrån namn</span><span class="sxs-lookup"><span data-stu-id="b5040-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="b5040-113">Det här kommandot tar bort den angivna princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="b5040-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="b5040-114">Exempel 2: ta bort princip definitionen efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="b5040-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="b5040-115">Det första kommandot hämtar princip definitionen med namnet VMPolicyDefinition med hjälp av Get-AzureRmPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5040-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="b5040-116">Kommandot sparar det i $PolicyDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="b5040-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="b5040-117">Det andra kommandot tar bort princip definitionen som identifieras av egenskapen **ResourceID** för $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="b5040-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="b5040-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5040-118">PARAMETERS</span></span>

### <span data-ttu-id="b5040-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b5040-119">-ApiVersion</span></span>
<span data-ttu-id="b5040-120">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="b5040-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b5040-121">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="b5040-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b5040-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5040-122">-DefaultProfile</span></span>
<span data-ttu-id="b5040-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b5040-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5040-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b5040-124">-Force</span></span>
<span data-ttu-id="b5040-125">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b5040-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b5040-126">-ID</span><span class="sxs-lookup"><span data-stu-id="b5040-126">-Id</span></span>
<span data-ttu-id="b5040-127">Anger det fullständiga resurs-ID för princip definitionen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="b5040-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b5040-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b5040-128">-InformationAction</span></span>
<span data-ttu-id="b5040-129">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="b5040-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="b5040-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b5040-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b5040-131">Vidare</span><span class="sxs-lookup"><span data-stu-id="b5040-131">Continue</span></span>
- <span data-ttu-id="b5040-132">Över</span><span class="sxs-lookup"><span data-stu-id="b5040-132">Ignore</span></span>
- <span data-ttu-id="b5040-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="b5040-133">Inquire</span></span>
- <span data-ttu-id="b5040-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b5040-134">SilentlyContinue</span></span>
- <span data-ttu-id="b5040-135">Stanna</span><span class="sxs-lookup"><span data-stu-id="b5040-135">Stop</span></span>
- <span data-ttu-id="b5040-136">Avbryt</span><span class="sxs-lookup"><span data-stu-id="b5040-136">Suspend</span></span>

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

### <span data-ttu-id="b5040-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b5040-137">-InformationVariable</span></span>
<span data-ttu-id="b5040-138">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="b5040-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b5040-139">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="b5040-139">-ManagementGroupName</span></span>
<span data-ttu-id="b5040-140">Namnet på hanterings gruppen för princip definitionen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b5040-140">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="b5040-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="b5040-141">-Name</span></span>
<span data-ttu-id="b5040-142">Anger namnet på princip definitionen som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="b5040-142">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b5040-143">-För</span><span class="sxs-lookup"><span data-stu-id="b5040-143">-Pre</span></span>
<span data-ttu-id="b5040-144">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="b5040-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b5040-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b5040-145">-SubscriptionId</span></span>
<span data-ttu-id="b5040-146">Abonnemangs-ID för princip definitionen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b5040-146">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="b5040-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b5040-147">-Confirm</span></span>
<span data-ttu-id="b5040-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b5040-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5040-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5040-149">-WhatIf</span></span>
<span data-ttu-id="b5040-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b5040-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5040-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b5040-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5040-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5040-152">CommonParameters</span></span>
<span data-ttu-id="b5040-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5040-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5040-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5040-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5040-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5040-155">INPUTS</span></span>

## <span data-ttu-id="b5040-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5040-156">OUTPUTS</span></span>

## <span data-ttu-id="b5040-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5040-157">NOTES</span></span>

## <span data-ttu-id="b5040-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5040-158">RELATED LINKS</span></span>

[<span data-ttu-id="b5040-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b5040-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="b5040-160">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b5040-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="b5040-161">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b5040-161">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


