---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 0caf541aeadcbf2617ae5d31d0dfaf69e432e888
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583031"
---
# <span data-ttu-id="123d9-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="123d9-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="123d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="123d9-102">SYNOPSIS</span></span>
<span data-ttu-id="123d9-103">Verifierar en distribution av en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="123d9-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="123d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="123d9-104">SYNTAX</span></span>

### <span data-ttu-id="123d9-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="123d9-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="123d9-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="123d9-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="123d9-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="123d9-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="123d9-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="123d9-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="123d9-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="123d9-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="123d9-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="123d9-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="123d9-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="123d9-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="123d9-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="123d9-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="123d9-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="123d9-113">DESCRIPTION</span></span>
<span data-ttu-id="123d9-114">**Test-AzureRmResourceGroupDeployment** cmdlet bestämmer om en Azure Resource Group-distributionsmall och dess parameter värden är giltiga.</span><span class="sxs-lookup"><span data-stu-id="123d9-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="123d9-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="123d9-115">EXAMPLES</span></span>

## <span data-ttu-id="123d9-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="123d9-116">PARAMETERS</span></span>

### <span data-ttu-id="123d9-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="123d9-117">-ApiVersion</span></span>
<span data-ttu-id="123d9-118">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="123d9-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="123d9-119">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="123d9-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="123d9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="123d9-120">-DefaultProfile</span></span>
<span data-ttu-id="123d9-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="123d9-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="123d9-122">-Mode</span><span class="sxs-lookup"><span data-stu-id="123d9-122">-Mode</span></span>
<span data-ttu-id="123d9-123">Anger distributions läget.</span><span class="sxs-lookup"><span data-stu-id="123d9-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="123d9-124">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="123d9-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="123d9-125">Stegvis</span><span class="sxs-lookup"><span data-stu-id="123d9-125">Incremental</span></span>
- <span data-ttu-id="123d9-126">Kunna</span><span class="sxs-lookup"><span data-stu-id="123d9-126">Complete</span></span>

```yaml
Type: DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="123d9-127">-För</span><span class="sxs-lookup"><span data-stu-id="123d9-127">-Pre</span></span>
<span data-ttu-id="123d9-128">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="123d9-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="123d9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="123d9-129">-ResourceGroupName</span></span>
<span data-ttu-id="123d9-130">Anger namnet på den resurs grupp som ska testas.</span><span class="sxs-lookup"><span data-stu-id="123d9-130">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="123d9-131">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="123d9-131">-TemplateFile</span></span>
<span data-ttu-id="123d9-132">Anger den fullständiga sökvägen till en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="123d9-132">Specifies the full path of a JSON template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="123d9-133">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="123d9-133">-TemplateParameterFile</span></span>
<span data-ttu-id="123d9-134">Anger den fullständiga sökvägen till en JSON-fil som innehåller namn och värden för mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="123d9-134">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="123d9-135">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="123d9-135">-TemplateParameterObject</span></span>
<span data-ttu-id="123d9-136">Anger en hash-tabell med namn och värden för Mallkategorier.</span><span class="sxs-lookup"><span data-stu-id="123d9-136">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="123d9-137">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="123d9-137">-TemplateParameterUri</span></span>
<span data-ttu-id="123d9-138">Anger URI-filen för en mall.</span><span class="sxs-lookup"><span data-stu-id="123d9-138">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="123d9-139">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="123d9-139">-TemplateUri</span></span>
<span data-ttu-id="123d9-140">Anger URI för en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="123d9-140">Specifies the URI of a JSON template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="123d9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="123d9-141">CommonParameters</span></span>
<span data-ttu-id="123d9-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="123d9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="123d9-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="123d9-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="123d9-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="123d9-144">INPUTS</span></span>

### <span data-ttu-id="123d9-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="123d9-145">None</span></span>
<span data-ttu-id="123d9-146">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="123d9-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="123d9-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="123d9-147">OUTPUTS</span></span>

### <span data-ttu-id="123d9-148">System. Collections. Generic. list ' 1 [Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceManagerError]</span><span class="sxs-lookup"><span data-stu-id="123d9-148">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError]</span></span>

## <span data-ttu-id="123d9-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="123d9-149">NOTES</span></span>

## <span data-ttu-id="123d9-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="123d9-150">RELATED LINKS</span></span>

[<span data-ttu-id="123d9-151">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="123d9-151">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="123d9-152">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="123d9-152">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="123d9-153">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="123d9-153">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="123d9-154">Stopp-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="123d9-154">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


