---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeploymentOperation.md
ms.openlocfilehash: 557aa312200a2e5c49e33f8a176079ee4b27b629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575537"
---
# <span data-ttu-id="47a0b-101">Get-AzureRmResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="47a0b-101">Get-AzureRmResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="47a0b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="47a0b-103">Får distributions åtgärden för resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="47a0b-103">Gets the resource group deployment operation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47a0b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47a0b-104">SYNTAX</span></span>

```
Get-AzureRmResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="47a0b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47a0b-105">DESCRIPTION</span></span>
<span data-ttu-id="47a0b-106">Cmdleten **Get-AzureRmResourceGroupDeploymentOperation** innehåller alla åtgärder som ingick i en distribution för att hjälpa dig att identifiera och ge mer information om de exakta operationer som misslyckats för en viss distribution.</span><span class="sxs-lookup"><span data-stu-id="47a0b-106">The **Get-AzureRmResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="47a0b-107">Den kan också Visa svaret och innehållet i begäran för varje distributions åtgärd.</span><span class="sxs-lookup"><span data-stu-id="47a0b-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="47a0b-108">Det här är samma information som anges i distributions informationen på portalen.</span><span class="sxs-lookup"><span data-stu-id="47a0b-108">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="47a0b-109">För att få begäran och svars innehållet aktiverar du inställningen när du skickar en distribution via **New-AzureRmResourceGroupDeployment**.</span><span class="sxs-lookup"><span data-stu-id="47a0b-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzureRmResourceGroupDeployment**.</span></span>
<span data-ttu-id="47a0b-110">Det kan vara möjligt att logga in och Visa hemligheter som lösen ord som används i resurs egenskapen eller **listKeys** operationer och sedan returneras när du hämtar distributions åtgärderna.</span><span class="sxs-lookup"><span data-stu-id="47a0b-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="47a0b-111">Om du vill ha mer information om den här inställningen och hur du aktiverar den kan du läsa distribuera mallar för New-AzureRmResourceGroupDeployment och fel söknings verktyg</span><span class="sxs-lookup"><span data-stu-id="47a0b-111">For more on this setting and how to enable it, see New-AzureRmResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="47a0b-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47a0b-112">EXAMPLES</span></span>

### <span data-ttu-id="47a0b-113">Get1</span><span class="sxs-lookup"><span data-stu-id="47a0b-113">Get1</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="47a0b-114">Får distributions åtgärd med namnet "test" under resurs gruppen "test"</span><span class="sxs-lookup"><span data-stu-id="47a0b-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="47a0b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47a0b-115">PARAMETERS</span></span>

### <span data-ttu-id="47a0b-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="47a0b-116">-ApiVersion</span></span>
<span data-ttu-id="47a0b-117">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="47a0b-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="47a0b-118">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="47a0b-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="47a0b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47a0b-119">-DefaultProfile</span></span>
<span data-ttu-id="47a0b-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="47a0b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47a0b-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="47a0b-121">-DeploymentName</span></span>
<span data-ttu-id="47a0b-122">Distributions namn.</span><span class="sxs-lookup"><span data-stu-id="47a0b-122">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a0b-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="47a0b-123">-InformationAction</span></span>
<span data-ttu-id="47a0b-124">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="47a0b-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="47a0b-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="47a0b-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="47a0b-126">Vidare</span><span class="sxs-lookup"><span data-stu-id="47a0b-126">Continue</span></span>
- <span data-ttu-id="47a0b-127">Över</span><span class="sxs-lookup"><span data-stu-id="47a0b-127">Ignore</span></span>
- <span data-ttu-id="47a0b-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="47a0b-128">Inquire</span></span>
- <span data-ttu-id="47a0b-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="47a0b-129">SilentlyContinue</span></span>
- <span data-ttu-id="47a0b-130">Stanna</span><span class="sxs-lookup"><span data-stu-id="47a0b-130">Stop</span></span>
- <span data-ttu-id="47a0b-131">Avbryt</span><span class="sxs-lookup"><span data-stu-id="47a0b-131">Suspend</span></span>

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

### <span data-ttu-id="47a0b-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="47a0b-132">-InformationVariable</span></span>
<span data-ttu-id="47a0b-133">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="47a0b-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="47a0b-134">-För</span><span class="sxs-lookup"><span data-stu-id="47a0b-134">-Pre</span></span>
<span data-ttu-id="47a0b-135">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="47a0b-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="47a0b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47a0b-136">-ResourceGroupName</span></span>
<span data-ttu-id="47a0b-137">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="47a0b-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a0b-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47a0b-138">-SubscriptionId</span></span>
<span data-ttu-id="47a0b-139">Abonnemanget som ska användas.</span><span class="sxs-lookup"><span data-stu-id="47a0b-139">The subscription to use.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47a0b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47a0b-140">CommonParameters</span></span>
<span data-ttu-id="47a0b-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47a0b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47a0b-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47a0b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47a0b-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47a0b-143">INPUTS</span></span>

### <span data-ttu-id="47a0b-144">Ande</span><span class="sxs-lookup"><span data-stu-id="47a0b-144">Guid</span></span>
<span data-ttu-id="47a0b-145">Parametern ' SubscriptionId ' godkänner värdet för typen ' GUID ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="47a0b-145">Parameter 'SubscriptionId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="47a0b-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47a0b-146">OUTPUTS</span></span>

### <span data-ttu-id="47a0b-147">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="47a0b-147">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="47a0b-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47a0b-148">NOTES</span></span>

## <span data-ttu-id="47a0b-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47a0b-149">RELATED LINKS</span></span>