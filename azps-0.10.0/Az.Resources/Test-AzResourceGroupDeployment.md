---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-Azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 59bbe7c5309764c41f22aaa99dbb4d47a23f1ba8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923749"
---
# <span data-ttu-id="6e52e-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6e52e-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="6e52e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e52e-102">SYNOPSIS</span></span>
<span data-ttu-id="6e52e-103">Verifierar en distribution av en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6e52e-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="6e52e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e52e-104">SYNTAX</span></span>

### <span data-ttu-id="6e52e-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="6e52e-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateFile <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e52e-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="6e52e-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e52e-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="6e52e-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e52e-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="6e52e-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e52e-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="6e52e-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e52e-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="6e52e-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e52e-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="6e52e-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e52e-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="6e52e-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateUri <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e52e-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e52e-113">DESCRIPTION</span></span>
<span data-ttu-id="6e52e-114">**Test-AzResourceGroupDeployment** cmdlet bestämmer om en Azure Resource Group-distributionsmall och dess parameter värden är giltiga.</span><span class="sxs-lookup"><span data-stu-id="6e52e-114">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="6e52e-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e52e-115">EXAMPLES</span></span>

## <span data-ttu-id="6e52e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e52e-116">PARAMETERS</span></span>

### <span data-ttu-id="6e52e-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6e52e-117">-ApiVersion</span></span>
<span data-ttu-id="6e52e-118">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="6e52e-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="6e52e-119">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="6e52e-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="6e52e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e52e-120">-DefaultProfile</span></span>
<span data-ttu-id="6e52e-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6e52e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e52e-122">-Mode</span><span class="sxs-lookup"><span data-stu-id="6e52e-122">-Mode</span></span>
<span data-ttu-id="6e52e-123">Anger distributions läget.</span><span class="sxs-lookup"><span data-stu-id="6e52e-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="6e52e-124">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6e52e-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6e52e-125">Stegvis</span><span class="sxs-lookup"><span data-stu-id="6e52e-125">Incremental</span></span>
- <span data-ttu-id="6e52e-126">Kunna</span><span class="sxs-lookup"><span data-stu-id="6e52e-126">Complete</span></span>

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

### <span data-ttu-id="6e52e-127">-För</span><span class="sxs-lookup"><span data-stu-id="6e52e-127">-Pre</span></span>
<span data-ttu-id="6e52e-128">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="6e52e-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6e52e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e52e-129">-ResourceGroupName</span></span>
<span data-ttu-id="6e52e-130">Anger namnet på den resurs grupp som ska testas.</span><span class="sxs-lookup"><span data-stu-id="6e52e-130">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="6e52e-131">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="6e52e-131">-RollBackDeploymentName</span></span>
<span data-ttu-id="6e52e-132">Återställ till lyckad distribution med angivet namn i resurs gruppen, ska inte användas om-RollbackToLastDeployment används.</span><span class="sxs-lookup"><span data-stu-id="6e52e-132">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e52e-133">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="6e52e-133">-RollbackToLastDeployment</span></span>
<span data-ttu-id="6e52e-134">Återställ till den senaste lyckade distributionen i resurs gruppen, bör inte förekomma om-RollBackDeploymentName används.</span><span class="sxs-lookup"><span data-stu-id="6e52e-134">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="6e52e-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="6e52e-135">-TemplateFile</span></span>
<span data-ttu-id="6e52e-136">Anger den fullständiga sökvägen till en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="6e52e-136">Specifies the full path of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e52e-137">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="6e52e-137">-TemplateParameterFile</span></span>
<span data-ttu-id="6e52e-138">Anger den fullständiga sökvägen till en JSON-fil som innehåller namn och värden för mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="6e52e-138">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e52e-139">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="6e52e-139">-TemplateParameterObject</span></span>
<span data-ttu-id="6e52e-140">Anger en hash-tabell med namn och värden för Mallkategorier.</span><span class="sxs-lookup"><span data-stu-id="6e52e-140">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e52e-141">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="6e52e-141">-TemplateParameterUri</span></span>
<span data-ttu-id="6e52e-142">Anger URI-filen för en mall.</span><span class="sxs-lookup"><span data-stu-id="6e52e-142">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e52e-143">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="6e52e-143">-TemplateUri</span></span>
<span data-ttu-id="6e52e-144">Anger URI för en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="6e52e-144">Specifies the URI of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e52e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e52e-145">CommonParameters</span></span>
<span data-ttu-id="6e52e-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e52e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e52e-147">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e52e-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e52e-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e52e-148">INPUTS</span></span>

### <span data-ttu-id="6e52e-149">Ingen</span><span class="sxs-lookup"><span data-stu-id="6e52e-149">None</span></span>

## <span data-ttu-id="6e52e-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e52e-150">OUTPUTS</span></span>

### <span data-ttu-id="6e52e-151">Microsoft. Azure. commands. ResourceManager. Models. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="6e52e-151">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceManagerError</span></span>

## <span data-ttu-id="6e52e-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e52e-152">NOTES</span></span>

## <span data-ttu-id="6e52e-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e52e-153">RELATED LINKS</span></span>

[<span data-ttu-id="6e52e-154">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6e52e-154">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="6e52e-155">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6e52e-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="6e52e-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6e52e-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="6e52e-157">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6e52e-157">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

