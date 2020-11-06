---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: b357215bf2c4ba032ca44e37cc445e12606aeffe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577504"
---
# <span data-ttu-id="b3b1a-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b3b1a-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="b3b1a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3b1a-102">SYNOPSIS</span></span>
<span data-ttu-id="b3b1a-103">Verifierar en distribution av en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b3b1a-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3b1a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3b1a-104">SYNTAX</span></span>

### <span data-ttu-id="b3b1a-105">Distribution via mallfil utan parametrar (standard)</span><span class="sxs-lookup"><span data-stu-id="b3b1a-105">Deployment via template file without parameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b1a-106">Distribution via mall-och mallparametrar-objekt</span><span class="sxs-lookup"><span data-stu-id="b3b1a-106">Deployment via template file and template parameters object</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b1a-107">Distribution via mallens URI och mallparametrar-objekt</span><span class="sxs-lookup"><span data-stu-id="b3b1a-107">Deployment via template uri and template parameters object</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b1a-108">Distribution via mallfiler och mallparametrar fil</span><span class="sxs-lookup"><span data-stu-id="b3b1a-108">Deployment via template file and template parameters file</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b1a-109">Distribution via mallens URI och mallparametrar</span><span class="sxs-lookup"><span data-stu-id="b3b1a-109">Deployment via template uri and template parameters file</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b1a-110">Distribution via mallfiler URI för parametrar</span><span class="sxs-lookup"><span data-stu-id="b3b1a-110">Deployment via template file template parameters uri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b1a-111">Distribution via mall-URI och mallparametrar URI</span><span class="sxs-lookup"><span data-stu-id="b3b1a-111">Deployment via template uri and template parameters uri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b1a-112">Distribution via mall-URI utan parametrar</span><span class="sxs-lookup"><span data-stu-id="b3b1a-112">Deployment via template uri without parameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3b1a-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3b1a-113">DESCRIPTION</span></span>
<span data-ttu-id="b3b1a-114">**Test-AzureRmResourceGroupDeployment** cmdlet bestämmer om en Azure Resource Group-distributionsmall och dess parameter värden är giltiga.</span><span class="sxs-lookup"><span data-stu-id="b3b1a-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="b3b1a-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3b1a-115">EXAMPLES</span></span>

## <span data-ttu-id="b3b1a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3b1a-116">PARAMETERS</span></span>

### <span data-ttu-id="b3b1a-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b3b1a-117">-ApiVersion</span></span>
<span data-ttu-id="b3b1a-118">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="b3b1a-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b3b1a-119">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="b3b1a-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="b3b1a-120">-Mode</span><span class="sxs-lookup"><span data-stu-id="b3b1a-120">-Mode</span></span>
<span data-ttu-id="b3b1a-121">Anger distributions läget.</span><span class="sxs-lookup"><span data-stu-id="b3b1a-121">Specifies the deployment mode.</span></span>
<span data-ttu-id="b3b1a-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b3b1a-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b3b1a-123">Stegvis</span><span class="sxs-lookup"><span data-stu-id="b3b1a-123">Incremental</span></span>
- <span data-ttu-id="b3b1a-124">Kunna</span><span class="sxs-lookup"><span data-stu-id="b3b1a-124">Complete</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b1a-125">-För</span><span class="sxs-lookup"><span data-stu-id="b3b1a-125">-Pre</span></span>
<span data-ttu-id="b3b1a-126">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="b3b1a-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b3b1a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3b1a-127">-ResourceGroupName</span></span>
<span data-ttu-id="b3b1a-128">Anger namnet på den resurs grupp som ska testas.</span><span class="sxs-lookup"><span data-stu-id="b3b1a-128">Specifies the name of the resource group to test.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b1a-129">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="b3b1a-129">-TemplateFile</span></span>
<span data-ttu-id="b3b1a-130">Anger den fullständiga sökvägen till en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="b3b1a-130">Specifies the full path of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file without parameters, Deployment via template file and template parameters object, Deployment via template file and template parameters file, Deployment via template file template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b1a-131">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="b3b1a-131">-TemplateParameterFile</span></span>
<span data-ttu-id="b3b1a-132">Anger den fullständiga sökvägen till en JSON-fil som innehåller namn och värden för mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="b3b1a-132">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file and template parameters file, Deployment via template uri and template parameters file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b1a-133">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="b3b1a-133">-TemplateParameterObject</span></span>
<span data-ttu-id="b3b1a-134">Anger en hash-tabell med namn och värden för Mallkategorier.</span><span class="sxs-lookup"><span data-stu-id="b3b1a-134">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Deployment via template file and template parameters object, Deployment via template uri and template parameters object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b1a-135">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="b3b1a-135">-TemplateParameterUri</span></span>
<span data-ttu-id="b3b1a-136">Anger URI-filen för en mall.</span><span class="sxs-lookup"><span data-stu-id="b3b1a-136">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file template parameters uri, Deployment via template uri and template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b1a-137">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b3b1a-137">-TemplateUri</span></span>
<span data-ttu-id="b3b1a-138">Anger URI för en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="b3b1a-138">Specifies the URI of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template uri and template parameters object, Deployment via template uri and template parameters file, Deployment via template uri and template parameters uri, Deployment via template uri without parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b1a-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3b1a-139">-DefaultProfile</span></span>
<span data-ttu-id="b3b1a-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b3b1a-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3b1a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b1a-141">CommonParameters</span></span>
<span data-ttu-id="b3b1a-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3b1a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b1a-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3b1a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b1a-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3b1a-144">INPUTS</span></span>

## <span data-ttu-id="b3b1a-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3b1a-145">OUTPUTS</span></span>

### <span data-ttu-id="b3b1a-146">System. Collections. Generic. list ' 1 [Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceManagerError]</span><span class="sxs-lookup"><span data-stu-id="b3b1a-146">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError]</span></span>

## <span data-ttu-id="b3b1a-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3b1a-147">NOTES</span></span>

## <span data-ttu-id="b3b1a-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3b1a-148">RELATED LINKS</span></span>

[<span data-ttu-id="b3b1a-149">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b3b1a-149">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b3b1a-150">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b3b1a-150">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b3b1a-151">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b3b1a-151">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b3b1a-152">Stopp-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b3b1a-152">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


