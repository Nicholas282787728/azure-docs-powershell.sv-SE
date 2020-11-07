---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 68c4f94ea4fee91c03ab0c65cbcba0f025c3c43b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755372"
---
# <span data-ttu-id="1fc00-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1fc00-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="1fc00-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1fc00-102">SYNOPSIS</span></span>
<span data-ttu-id="1fc00-103">Tar bort en princip definition.</span><span class="sxs-lookup"><span data-stu-id="1fc00-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fc00-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1fc00-104">SYNTAX</span></span>

### <span data-ttu-id="1fc00-105">RemoveByPolicyDefinitionName (standard)</span><span class="sxs-lookup"><span data-stu-id="1fc00-105">RemoveByPolicyDefinitionName (Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fc00-106">RemoveByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="1fc00-106">RemoveByPolicyDefinitionId</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fc00-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1fc00-107">DESCRIPTION</span></span>
<span data-ttu-id="1fc00-108">Cmdleten **Remove-AzureRmPolicyDefinition** tar bort en princip definition.</span><span class="sxs-lookup"><span data-stu-id="1fc00-108">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="1fc00-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1fc00-109">EXAMPLES</span></span>

### <span data-ttu-id="1fc00-110">Exempel 1: ta bort princip definitionen utifrån namn</span><span class="sxs-lookup"><span data-stu-id="1fc00-110">Example 1: Remove the policy definition by name</span></span>
```
PS C:\>Remove-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="1fc00-111">Det här kommandot tar bort den angivna princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="1fc00-111">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="1fc00-112">Exempel 2: ta bort princip definitionen efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="1fc00-112">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition" 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="1fc00-113">Det första kommandot hämtar princip definitionen med namnet VMPolicyDefinition med hjälp av Get-AzureRmPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fc00-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="1fc00-114">Kommandot sparar det i $PolicyDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="1fc00-114">The command stores it in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="1fc00-115">Det andra kommandot tar bort princip definitionen som identifieras av egenskapen **ResourceID** för $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="1fc00-115">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="1fc00-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1fc00-116">PARAMETERS</span></span>

### <span data-ttu-id="1fc00-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1fc00-117">-ApiVersion</span></span>
<span data-ttu-id="1fc00-118">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="1fc00-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="1fc00-119">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="1fc00-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc00-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fc00-120">-DefaultProfile</span></span>
<span data-ttu-id="1fc00-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1fc00-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1fc00-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1fc00-122">-Force</span></span>
<span data-ttu-id="1fc00-123">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="1fc00-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1fc00-124">-ID</span><span class="sxs-lookup"><span data-stu-id="1fc00-124">-Id</span></span>
<span data-ttu-id="1fc00-125">Anger det fullständiga resurs-ID för princip definitionen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="1fc00-125">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fc00-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1fc00-126">-InformationAction</span></span>
<span data-ttu-id="1fc00-127">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="1fc00-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1fc00-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1fc00-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1fc00-129">Vidare</span><span class="sxs-lookup"><span data-stu-id="1fc00-129">Continue</span></span>
- <span data-ttu-id="1fc00-130">Över</span><span class="sxs-lookup"><span data-stu-id="1fc00-130">Ignore</span></span>
- <span data-ttu-id="1fc00-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="1fc00-131">Inquire</span></span>
- <span data-ttu-id="1fc00-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1fc00-132">SilentlyContinue</span></span>
- <span data-ttu-id="1fc00-133">Stanna</span><span class="sxs-lookup"><span data-stu-id="1fc00-133">Stop</span></span>
- <span data-ttu-id="1fc00-134">Avbryt</span><span class="sxs-lookup"><span data-stu-id="1fc00-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc00-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1fc00-135">-InformationVariable</span></span>
<span data-ttu-id="1fc00-136">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="1fc00-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc00-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="1fc00-137">-Name</span></span>
<span data-ttu-id="1fc00-138">Anger namnet på princip definitionen som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="1fc00-138">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyDefinitionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fc00-139">-För</span><span class="sxs-lookup"><span data-stu-id="1fc00-139">-Pre</span></span>
<span data-ttu-id="1fc00-140">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="1fc00-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1fc00-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1fc00-141">-Confirm</span></span>
<span data-ttu-id="1fc00-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1fc00-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc00-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fc00-143">-WhatIf</span></span>
<span data-ttu-id="1fc00-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1fc00-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fc00-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1fc00-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc00-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fc00-146">CommonParameters</span></span>
<span data-ttu-id="1fc00-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fc00-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fc00-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fc00-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fc00-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1fc00-149">INPUTS</span></span>

### <span data-ttu-id="1fc00-150">Ingen</span><span class="sxs-lookup"><span data-stu-id="1fc00-150">None</span></span>
<span data-ttu-id="1fc00-151">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="1fc00-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1fc00-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1fc00-152">OUTPUTS</span></span>

### <span data-ttu-id="1fc00-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1fc00-153">System.Boolean</span></span>

## <span data-ttu-id="1fc00-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1fc00-154">NOTES</span></span>

## <span data-ttu-id="1fc00-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1fc00-155">RELATED LINKS</span></span>

[<span data-ttu-id="1fc00-156">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1fc00-156">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="1fc00-157">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1fc00-157">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="1fc00-158">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1fc00-158">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


