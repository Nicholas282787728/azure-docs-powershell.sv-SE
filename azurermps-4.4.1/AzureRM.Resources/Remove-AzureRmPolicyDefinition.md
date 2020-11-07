---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 46323b260330ca84ee1ac2426ee7b6e2ab474f21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757469"
---
# <span data-ttu-id="3be33-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3be33-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="3be33-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3be33-102">SYNOPSIS</span></span>
<span data-ttu-id="3be33-103">Tar bort en princip definition.</span><span class="sxs-lookup"><span data-stu-id="3be33-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3be33-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3be33-104">SYNTAX</span></span>

### <span data-ttu-id="3be33-105">Parametern för princip definitions namn.</span><span class="sxs-lookup"><span data-stu-id="3be33-105">The policy definition name parameter set.</span></span> <span data-ttu-id="3be33-106">Vis</span><span class="sxs-lookup"><span data-stu-id="3be33-106">(Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3be33-107">Parameter uppsättning för princip Definitions-ID.</span><span class="sxs-lookup"><span data-stu-id="3be33-107">The policy definition Id parameter set.</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3be33-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3be33-108">DESCRIPTION</span></span>
<span data-ttu-id="3be33-109">Cmdleten **Remove-AzureRmPolicyDefinition** tar bort en princip definition.</span><span class="sxs-lookup"><span data-stu-id="3be33-109">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="3be33-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3be33-110">EXAMPLES</span></span>

### <span data-ttu-id="3be33-111">Exempel 1: ta bort princip definitionen utifrån namn</span><span class="sxs-lookup"><span data-stu-id="3be33-111">Example 1: Remove the policy definition by name</span></span>
```
PS C:\>Remove-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="3be33-112">Det här kommandot tar bort den angivna princip definitionen.</span><span class="sxs-lookup"><span data-stu-id="3be33-112">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="3be33-113">Exempel 2: ta bort princip definitionen efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="3be33-113">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition" 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="3be33-114">Det första kommandot hämtar princip definitionen med namnet VMPolicyDefinition med hjälp av Get-AzureRmPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3be33-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="3be33-115">Kommandot sparar det i $PolicyDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="3be33-115">The command stores it in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="3be33-116">Det andra kommandot tar bort princip definitionen som identifieras av egenskapen **ResourceID** för $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="3be33-116">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="3be33-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3be33-117">PARAMETERS</span></span>

### <span data-ttu-id="3be33-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3be33-118">-ApiVersion</span></span>
<span data-ttu-id="3be33-119">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3be33-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3be33-120">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="3be33-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="3be33-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3be33-121">-Force</span></span>
<span data-ttu-id="3be33-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3be33-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3be33-123">-ID</span><span class="sxs-lookup"><span data-stu-id="3be33-123">-Id</span></span>
<span data-ttu-id="3be33-124">Anger det fullständiga resurs-ID för princip definitionen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="3be33-124">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3be33-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3be33-125">-InformationAction</span></span>
<span data-ttu-id="3be33-126">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="3be33-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3be33-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3be33-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3be33-128">Vidare</span><span class="sxs-lookup"><span data-stu-id="3be33-128">Continue</span></span>
- <span data-ttu-id="3be33-129">Över</span><span class="sxs-lookup"><span data-stu-id="3be33-129">Ignore</span></span>
- <span data-ttu-id="3be33-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="3be33-130">Inquire</span></span>
- <span data-ttu-id="3be33-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3be33-131">SilentlyContinue</span></span>
- <span data-ttu-id="3be33-132">Stanna</span><span class="sxs-lookup"><span data-stu-id="3be33-132">Stop</span></span>
- <span data-ttu-id="3be33-133">Avbryt</span><span class="sxs-lookup"><span data-stu-id="3be33-133">Suspend</span></span>

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

### <span data-ttu-id="3be33-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3be33-134">-InformationVariable</span></span>
<span data-ttu-id="3be33-135">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="3be33-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3be33-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="3be33-136">-Name</span></span>
<span data-ttu-id="3be33-137">Anger namnet på princip definitionen som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="3be33-137">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3be33-138">-För</span><span class="sxs-lookup"><span data-stu-id="3be33-138">-Pre</span></span>
<span data-ttu-id="3be33-139">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3be33-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3be33-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3be33-140">-Confirm</span></span>
<span data-ttu-id="3be33-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3be33-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3be33-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3be33-142">-WhatIf</span></span>
<span data-ttu-id="3be33-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3be33-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3be33-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3be33-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3be33-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3be33-145">-DefaultProfile</span></span>
<span data-ttu-id="3be33-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3be33-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3be33-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3be33-147">CommonParameters</span></span>
<span data-ttu-id="3be33-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3be33-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3be33-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3be33-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3be33-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3be33-150">INPUTS</span></span>

## <span data-ttu-id="3be33-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3be33-151">OUTPUTS</span></span>

### <span data-ttu-id="3be33-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3be33-152">System.Boolean</span></span>

## <span data-ttu-id="3be33-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3be33-153">NOTES</span></span>

## <span data-ttu-id="3be33-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3be33-154">RELATED LINKS</span></span>

[<span data-ttu-id="3be33-155">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3be33-155">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="3be33-156">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3be33-156">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="3be33-157">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3be33-157">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


