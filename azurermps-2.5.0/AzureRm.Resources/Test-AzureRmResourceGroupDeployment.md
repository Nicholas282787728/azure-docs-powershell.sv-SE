---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 97fbda90b27cbfabca8cbfd21c5bf375b86f7adb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930033"
---
# <span data-ttu-id="25378-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="25378-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="25378-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25378-102">SYNOPSIS</span></span>
<span data-ttu-id="25378-103">Verifierar en distribution av en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="25378-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25378-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25378-104">SYNTAX</span></span>

### <span data-ttu-id="25378-105">ByTemplateFileWithNoParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="25378-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateFile <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25378-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="25378-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25378-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="25378-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25378-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="25378-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25378-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="25378-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25378-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="25378-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25378-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="25378-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25378-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="25378-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateUri <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25378-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25378-113">DESCRIPTION</span></span>
<span data-ttu-id="25378-114">**Test-AzureRmResourceGroupDeployment** cmdlet bestämmer om en Azure Resource Group-distributionsmall och dess parameter värden är giltiga.</span><span class="sxs-lookup"><span data-stu-id="25378-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="25378-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25378-115">EXAMPLES</span></span>

## <span data-ttu-id="25378-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25378-116">PARAMETERS</span></span>

### <span data-ttu-id="25378-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="25378-117">-ApiVersion</span></span>
<span data-ttu-id="25378-118">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="25378-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="25378-119">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="25378-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="25378-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25378-120">-DefaultProfile</span></span>
<span data-ttu-id="25378-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="25378-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25378-122">-Mode</span><span class="sxs-lookup"><span data-stu-id="25378-122">-Mode</span></span>
<span data-ttu-id="25378-123">Anger distributions läget.</span><span class="sxs-lookup"><span data-stu-id="25378-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="25378-124">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="25378-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="25378-125">Stegvis</span><span class="sxs-lookup"><span data-stu-id="25378-125">Incremental</span></span>
- <span data-ttu-id="25378-126">Kunna</span><span class="sxs-lookup"><span data-stu-id="25378-126">Complete</span></span>

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

### <span data-ttu-id="25378-127">-För</span><span class="sxs-lookup"><span data-stu-id="25378-127">-Pre</span></span>
<span data-ttu-id="25378-128">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="25378-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="25378-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25378-129">-ResourceGroupName</span></span>
<span data-ttu-id="25378-130">Anger namnet på den resurs grupp som ska testas.</span><span class="sxs-lookup"><span data-stu-id="25378-130">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="25378-131">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="25378-131">-RollBackDeploymentName</span></span>
<span data-ttu-id="25378-132">Återställ till lyckad distribution med angivet namn i resurs gruppen, ska inte användas om-RollbackToLastDeployment används.</span><span class="sxs-lookup"><span data-stu-id="25378-132">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="25378-133">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="25378-133">-RollbackToLastDeployment</span></span>
<span data-ttu-id="25378-134">Återställ till den senaste lyckade distributionen i resurs gruppen, bör inte förekomma om-RollBackDeploymentName används.</span><span class="sxs-lookup"><span data-stu-id="25378-134">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="25378-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="25378-135">-TemplateFile</span></span>
<span data-ttu-id="25378-136">Anger den fullständiga sökvägen till en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="25378-136">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="25378-137">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="25378-137">-TemplateParameterFile</span></span>
<span data-ttu-id="25378-138">Anger den fullständiga sökvägen till en JSON-fil som innehåller namn och värden för mallparametrar.</span><span class="sxs-lookup"><span data-stu-id="25378-138">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="25378-139">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="25378-139">-TemplateParameterObject</span></span>
<span data-ttu-id="25378-140">Anger en hash-tabell med namn och värden för Mallkategorier.</span><span class="sxs-lookup"><span data-stu-id="25378-140">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="25378-141">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="25378-141">-TemplateParameterUri</span></span>
<span data-ttu-id="25378-142">Anger URI-filen för en mall.</span><span class="sxs-lookup"><span data-stu-id="25378-142">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="25378-143">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="25378-143">-TemplateUri</span></span>
<span data-ttu-id="25378-144">Anger URI för en JSON-mallfil.</span><span class="sxs-lookup"><span data-stu-id="25378-144">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="25378-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25378-145">CommonParameters</span></span>
<span data-ttu-id="25378-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25378-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25378-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25378-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25378-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25378-148">INPUTS</span></span>

### <span data-ttu-id="25378-149">Ingen</span><span class="sxs-lookup"><span data-stu-id="25378-149">None</span></span>

## <span data-ttu-id="25378-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25378-150">OUTPUTS</span></span>

### <span data-ttu-id="25378-151">Microsoft. Azure. commands. ResourceManager. Models. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="25378-151">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceManagerError</span></span>

## <span data-ttu-id="25378-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25378-152">NOTES</span></span>

## <span data-ttu-id="25378-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25378-153">RELATED LINKS</span></span>

[<span data-ttu-id="25378-154">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="25378-154">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="25378-155">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="25378-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="25378-156">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="25378-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="25378-157">Stopp-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="25378-157">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


