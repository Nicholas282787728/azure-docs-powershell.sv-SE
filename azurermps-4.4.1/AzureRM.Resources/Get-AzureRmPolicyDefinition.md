---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: 63ab8e9004b993429af31cb54e360c0b6d9854fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583795"
---
# <span data-ttu-id="d0273-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d0273-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="d0273-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0273-102">SYNOPSIS</span></span>
<span data-ttu-id="d0273-103">Hämtar princip definitioner.</span><span class="sxs-lookup"><span data-stu-id="d0273-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0273-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0273-104">SYNTAX</span></span>

### <span data-ttu-id="d0273-105">Parameter uppsättning för listan Alla princip definitioner.</span><span class="sxs-lookup"><span data-stu-id="d0273-105">The list all policy definitions parameter set.</span></span> <span data-ttu-id="d0273-106">Vis</span><span class="sxs-lookup"><span data-stu-id="d0273-106">(Default)</span></span>
```
Get-AzureRmPolicyDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d0273-107">Parametern för princip definitions namn.</span><span class="sxs-lookup"><span data-stu-id="d0273-107">The policy definition name parameter set.</span></span>
```
Get-AzureRmPolicyDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d0273-108">Parameter uppsättning för princip Definitions-ID.</span><span class="sxs-lookup"><span data-stu-id="d0273-108">The policy definition Id parameter set.</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d0273-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0273-109">DESCRIPTION</span></span>
<span data-ttu-id="d0273-110">Cmdleten **Get-AzureRmPolicyDefinition** hämtar alla princip definitioner eller en specifik princip definition som identifieras med namn eller ID.</span><span class="sxs-lookup"><span data-stu-id="d0273-110">The **Get-AzureRmPolicyDefinition** cmdlet gets all the policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="d0273-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0273-111">EXAMPLES</span></span>

### <span data-ttu-id="d0273-112">Exempel 1: Hämta alla princip definitioner</span><span class="sxs-lookup"><span data-stu-id="d0273-112">Example 1: Get all policy definition</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition
```

<span data-ttu-id="d0273-113">Det här kommandot får alla princip definitioner.</span><span class="sxs-lookup"><span data-stu-id="d0273-113">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="d0273-114">Exempel 2: Hämta princip definition efter namn</span><span class="sxs-lookup"><span data-stu-id="d0273-114">Example 2: Get policy definition by name</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="d0273-115">Det här kommandot får princip definitionen med namnet VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="d0273-115">This command gets the policy definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="d0273-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0273-116">PARAMETERS</span></span>

### <span data-ttu-id="d0273-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d0273-117">-ApiVersion</span></span>
<span data-ttu-id="d0273-118">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="d0273-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d0273-119">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="d0273-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d0273-120">-ID</span><span class="sxs-lookup"><span data-stu-id="d0273-120">-Id</span></span>
<span data-ttu-id="d0273-121">Anger det fullständigt kvalificerade resurs-ID för princip definitionen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="d0273-121">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d0273-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d0273-122">-InformationAction</span></span>
<span data-ttu-id="d0273-123">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="d0273-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d0273-124">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d0273-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d0273-125">Vidare</span><span class="sxs-lookup"><span data-stu-id="d0273-125">Continue</span></span>
- <span data-ttu-id="d0273-126">Över</span><span class="sxs-lookup"><span data-stu-id="d0273-126">Ignore</span></span>
- <span data-ttu-id="d0273-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="d0273-127">Inquire</span></span>
- <span data-ttu-id="d0273-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d0273-128">SilentlyContinue</span></span>
- <span data-ttu-id="d0273-129">Stanna</span><span class="sxs-lookup"><span data-stu-id="d0273-129">Stop</span></span>
- <span data-ttu-id="d0273-130">Avbryt</span><span class="sxs-lookup"><span data-stu-id="d0273-130">Suspend</span></span>

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

### <span data-ttu-id="d0273-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d0273-131">-InformationVariable</span></span>
<span data-ttu-id="d0273-132">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="d0273-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d0273-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="d0273-133">-Name</span></span>
<span data-ttu-id="d0273-134">Anger namnet på den princip definition som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="d0273-134">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d0273-135">-För</span><span class="sxs-lookup"><span data-stu-id="d0273-135">-Pre</span></span>
<span data-ttu-id="d0273-136">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="d0273-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d0273-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0273-137">-DefaultProfile</span></span>
<span data-ttu-id="d0273-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0273-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0273-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0273-139">CommonParameters</span></span>
<span data-ttu-id="d0273-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0273-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0273-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0273-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0273-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0273-142">INPUTS</span></span>

## <span data-ttu-id="d0273-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0273-143">OUTPUTS</span></span>

### <span data-ttu-id="d0273-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d0273-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d0273-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0273-145">NOTES</span></span>

## <span data-ttu-id="d0273-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0273-146">RELATED LINKS</span></span>

[<span data-ttu-id="d0273-147">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d0273-147">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="d0273-148">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d0273-148">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="d0273-149">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d0273-149">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


