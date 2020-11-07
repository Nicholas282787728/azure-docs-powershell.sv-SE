---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicydefinition
schema: 2.0.0
ms.openlocfilehash: 5bd650583a933ba8d7ea56762c918d386b630c6c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930101"
---
# <span data-ttu-id="aa4ea-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="aa4ea-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="aa4ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aa4ea-102">SYNOPSIS</span></span>
<span data-ttu-id="aa4ea-103">Hämtar princip definitioner.</span><span class="sxs-lookup"><span data-stu-id="aa4ea-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa4ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aa4ea-104">SYNTAX</span></span>

### <span data-ttu-id="aa4ea-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="aa4ea-105">NameParameterSet (Default)</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="aa4ea-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa4ea-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="aa4ea-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa4ea-107">SubscriptionIdParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="aa4ea-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa4ea-108">IdParameterSet</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="aa4ea-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa4ea-109">BuiltinFilterParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="aa4ea-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa4ea-110">CustomFilterParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="aa4ea-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aa4ea-111">DESCRIPTION</span></span>
<span data-ttu-id="aa4ea-112">Cmdleten **Get-AzureRmPolicyDefinition** hämtar en samling princip definitioner eller en specifik princip definition som identifieras med namn eller ID.</span><span class="sxs-lookup"><span data-stu-id="aa4ea-112">The **Get-AzureRmPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="aa4ea-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aa4ea-113">EXAMPLES</span></span>

### <span data-ttu-id="aa4ea-114">Exempel 1: Hämta alla princip definitioner</span><span class="sxs-lookup"><span data-stu-id="aa4ea-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition
```

<span data-ttu-id="aa4ea-115">Det här kommandot får alla princip definitioner.</span><span class="sxs-lookup"><span data-stu-id="aa4ea-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="aa4ea-116">Exempel 2: Hämta princip definition från aktuell prenumeration efter namn</span><span class="sxs-lookup"><span data-stu-id="aa4ea-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="aa4ea-117">Det här kommandot hämtar princip definitionen med namnet VMPolicyDefinition från den aktuella standard prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="aa4ea-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="aa4ea-118">Exempel 3: Hämta princip definition från hanterings grupp efter namn</span><span class="sxs-lookup"><span data-stu-id="aa4ea-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="aa4ea-119">Det här kommandot hämtar princip definitionen med namnet VMPolicyDefinition från hanterings gruppen med namnet Dept42.</span><span class="sxs-lookup"><span data-stu-id="aa4ea-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="aa4ea-120">Exempel 4: Hämta alla inbyggda princip definitioner från abonnemang</span><span class="sxs-lookup"><span data-stu-id="aa4ea-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="aa4ea-121">Det här kommandot får alla inbyggda princip definitioner från prenumerationen med ID-3bf44b72-c631-427a-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="aa4ea-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

## <span data-ttu-id="aa4ea-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aa4ea-122">PARAMETERS</span></span>

### <span data-ttu-id="aa4ea-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="aa4ea-123">-ApiVersion</span></span>
<span data-ttu-id="aa4ea-124">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="aa4ea-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="aa4ea-125">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="aa4ea-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="aa4ea-126">-Inbyggt</span><span class="sxs-lookup"><span data-stu-id="aa4ea-126">-Builtin</span></span>
<span data-ttu-id="aa4ea-127">Begränsar resultat listan till endast inbyggda princip definitioner.</span><span class="sxs-lookup"><span data-stu-id="aa4ea-127">Limits list of results to only built-in policy definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BuiltinFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa4ea-128">-Anpassad</span><span class="sxs-lookup"><span data-stu-id="aa4ea-128">-Custom</span></span>
<span data-ttu-id="aa4ea-129">Begränsar listan med resultat till endast anpassade princip definitioner.</span><span class="sxs-lookup"><span data-stu-id="aa4ea-129">Limits list of results to only custom policy definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CustomFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa4ea-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa4ea-130">-DefaultProfile</span></span>
<span data-ttu-id="aa4ea-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="aa4ea-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa4ea-132">-ID</span><span class="sxs-lookup"><span data-stu-id="aa4ea-132">-Id</span></span>
<span data-ttu-id="aa4ea-133">Anger det fullständigt kvalificerade resurs-ID för princip definitionen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="aa4ea-133">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="aa4ea-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="aa4ea-134">-InformationAction</span></span>
<span data-ttu-id="aa4ea-135">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="aa4ea-135">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="aa4ea-136">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="aa4ea-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aa4ea-137">Vidare</span><span class="sxs-lookup"><span data-stu-id="aa4ea-137">Continue</span></span>
- <span data-ttu-id="aa4ea-138">Över</span><span class="sxs-lookup"><span data-stu-id="aa4ea-138">Ignore</span></span>
- <span data-ttu-id="aa4ea-139">Inquire</span><span class="sxs-lookup"><span data-stu-id="aa4ea-139">Inquire</span></span>
- <span data-ttu-id="aa4ea-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="aa4ea-140">SilentlyContinue</span></span>
- <span data-ttu-id="aa4ea-141">Stanna</span><span class="sxs-lookup"><span data-stu-id="aa4ea-141">Stop</span></span>
- <span data-ttu-id="aa4ea-142">Avbryt</span><span class="sxs-lookup"><span data-stu-id="aa4ea-142">Suspend</span></span>

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

### <span data-ttu-id="aa4ea-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="aa4ea-143">-InformationVariable</span></span>
<span data-ttu-id="aa4ea-144">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="aa4ea-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="aa4ea-145">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="aa4ea-145">-ManagementGroupName</span></span>
<span data-ttu-id="aa4ea-146">Namnet på hanterings gruppen för de princip definitioner som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="aa4ea-146">The name of the management group of the policy definition(s) to get.</span></span>

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

```yaml
Type: System.String
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa4ea-147">-Namn</span><span class="sxs-lookup"><span data-stu-id="aa4ea-147">-Name</span></span>
<span data-ttu-id="aa4ea-148">Anger namnet på den princip definition som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="aa4ea-148">Specifies the name of the policy definition that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa4ea-149">-För</span><span class="sxs-lookup"><span data-stu-id="aa4ea-149">-Pre</span></span>
<span data-ttu-id="aa4ea-150">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="aa4ea-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="aa4ea-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa4ea-151">-SubscriptionId</span></span>
<span data-ttu-id="aa4ea-152">Prenumerations-ID för de princip definitioner som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="aa4ea-152">The subscription ID of the policy definition(s) to get.</span></span>

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

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa4ea-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa4ea-153">CommonParameters</span></span>
<span data-ttu-id="aa4ea-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa4ea-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa4ea-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa4ea-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa4ea-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aa4ea-156">INPUTS</span></span>

## <span data-ttu-id="aa4ea-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aa4ea-157">OUTPUTS</span></span>

## <span data-ttu-id="aa4ea-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aa4ea-158">NOTES</span></span>

## <span data-ttu-id="aa4ea-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aa4ea-159">RELATED LINKS</span></span>

[<span data-ttu-id="aa4ea-160">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="aa4ea-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="aa4ea-161">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="aa4ea-161">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="aa4ea-162">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="aa4ea-162">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


