---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/import-azcontainerregistryimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
ms.openlocfilehash: 5fee8fec8d7b87629bfa46932662f430534fc695
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319591"
---
# <span data-ttu-id="3f5d6-101">Import-AzContainerRegistryImage</span><span class="sxs-lookup"><span data-stu-id="3f5d6-101">Import-AzContainerRegistryImage</span></span>

## <span data-ttu-id="3f5d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f5d6-102">SYNOPSIS</span></span>
<span data-ttu-id="3f5d6-103">Importera en bild från ett offentligt/Azure-register till ett Azure-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-103">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="3f5d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f5d6-104">SYNTAX</span></span>

### <span data-ttu-id="3f5d6-105">ImportImageByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="3f5d6-105">ImportImageByResourceId (Default)</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f5d6-106">ImportImageByResourceIdWithCredential</span><span class="sxs-lookup"><span data-stu-id="3f5d6-106">ImportImageByResourceIdWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-Username <String>] -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f5d6-107">ImportImageByRegistryUri</span><span class="sxs-lookup"><span data-stu-id="3f5d6-107">ImportImageByRegistryUri</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f5d6-108">ImportImageByRegistryUriWithCredential</span><span class="sxs-lookup"><span data-stu-id="3f5d6-108">ImportImageByRegistryUriWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-Username <String>] -Password <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f5d6-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f5d6-109">DESCRIPTION</span></span>
<span data-ttu-id="3f5d6-110">Importera en bild från ett offentligt/Azure-register till ett Azure-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-110">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="3f5d6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f5d6-111">EXAMPLES</span></span>

### <span data-ttu-id="3f5d6-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3f5d6-112">Example 1</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage library/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryUri docker.io -TargetTag busybox:latest
```

<span data-ttu-id="3f5d6-113">Importera upptaget till ACR.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-113">Import busybox to ACR.</span></span> <span data-ttu-id="3f5d6-114">Fotnot</span><span class="sxs-lookup"><span data-stu-id="3f5d6-114">Note:</span></span> 
* <span data-ttu-id="3f5d6-115">"bibliotek/" måste läggas till före käll bild.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-115">"library/" need to be add before source image.</span></span> <span data-ttu-id="3f5d6-116">"upptagen: senaste" => "biblioteket/upptagen: senaste"</span><span class="sxs-lookup"><span data-stu-id="3f5d6-116">"busybox:latest" => "library/busybox:latest"</span></span>
* <span data-ttu-id="3f5d6-117">Autentiseringsuppgifter krävs om käll registret inte är offentligt tillgängligt</span><span class="sxs-lookup"><span data-stu-id="3f5d6-117">Credential needed if source registry is not publicly available</span></span>

### <span data-ttu-id="3f5d6-118">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3f5d6-118">Example 2</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage $SourceRegistry.azurecr.io/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryResourceId $SourceACRID -TargetTag busybox:latest
```

<span data-ttu-id="3f5d6-119">Importera upptaget från source ACR till Target ACR.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-119">Import busybox from source ACR to target ACR.</span></span> <span data-ttu-id="3f5d6-120">Fotnot</span><span class="sxs-lookup"><span data-stu-id="3f5d6-120">Note:</span></span> 
* <span data-ttu-id="3f5d6-121">Autentiseringsuppgifter krävs om administratörs användaren för käll registret hade inaktiverats.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-121">Credential needed if admin user for source registry was disabled.</span></span>

## <span data-ttu-id="3f5d6-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f5d6-122">PARAMETERS</span></span>

### <span data-ttu-id="3f5d6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f5d6-123">-DefaultProfile</span></span>
<span data-ttu-id="3f5d6-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5d6-125">-Mode</span><span class="sxs-lookup"><span data-stu-id="3f5d6-125">-Mode</span></span>
<span data-ttu-id="3f5d6-126">När Force används skrivs alla befintliga målattribut ut.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-126">When Force, any existing target tags will be overwritten.</span></span>
<span data-ttu-id="3f5d6-127">Om det inte går att utföra operationen när kopieringen påbörjas Miss lyckas eventuella befintliga målattribut.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-127">When NoForce, any existing target tags will fail the operation before any copying begins.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Force, NoForce

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5d6-128">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="3f5d6-128">-Password</span></span>
<span data-ttu-id="3f5d6-129">Lösen ordet som används för att autentisera med käll registret.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-129">The password used to authenticate with the source registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5d6-130">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="3f5d6-130">-RegistryName</span></span>
<span data-ttu-id="3f5d6-131">Mål register namn.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-131">Target registry name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5d6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f5d6-132">-ResourceGroupName</span></span>
<span data-ttu-id="3f5d6-133">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-133">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5d6-134">-SourceImage</span><span class="sxs-lookup"><span data-stu-id="3f5d6-134">-SourceImage</span></span>
<span data-ttu-id="3f5d6-135">Käll bildens databas namn.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-135">Repository name of the source image.</span></span>

<span data-ttu-id="3f5d6-136">Ange en bild per databas (' Hej-världen ').</span><span class="sxs-lookup"><span data-stu-id="3f5d6-136">Specify an image by repository ('hello-world').</span></span>
<span data-ttu-id="3f5d6-137">Detta kommer att använda märket "senaste".</span><span class="sxs-lookup"><span data-stu-id="3f5d6-137">This will use the 'latest' tag.</span></span>

<span data-ttu-id="3f5d6-138">Ange en bild efter tagg (' Hej-världen: senaste ").</span><span class="sxs-lookup"><span data-stu-id="3f5d6-138">Specify an image by tag ('hello-world:latest').</span></span>

<span data-ttu-id="3f5d6-139">Ange en bild med SHA256 manifest sammandrag (' hello-world@sha256:abc123 ').</span><span class="sxs-lookup"><span data-stu-id="3f5d6-139">Specify an image by sha256-based manifest digest ('hello-world@sha256:abc123').</span></span>

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

### <span data-ttu-id="3f5d6-140">-SourceRegistryResourceId</span><span class="sxs-lookup"><span data-stu-id="3f5d6-140">-SourceRegistryResourceId</span></span>
<span data-ttu-id="3f5d6-141">Resurs-ID för käll-Azure Container-registret.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-141">The resource identifier of the source Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceId, ImportImageByResourceIdWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f5d6-142">-SourceRegistryUri</span><span class="sxs-lookup"><span data-stu-id="3f5d6-142">-SourceRegistryUri</span></span>
<span data-ttu-id="3f5d6-143">Adressen till käll registret (till exempel "mcr.microsoft.com").</span><span class="sxs-lookup"><span data-stu-id="3f5d6-143">The address of the source registry (e.g. 'mcr.microsoft.com').</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByRegistryUri, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f5d6-144">-TargetTag</span><span class="sxs-lookup"><span data-stu-id="3f5d6-144">-TargetTag</span></span>
<span data-ttu-id="3f5d6-145">Lista över strängar i formen repo \[ : tagg \] .</span><span class="sxs-lookup"><span data-stu-id="3f5d6-145">List of strings of the form repo\[:tag\].</span></span>
<span data-ttu-id="3f5d6-146">När tagg utelämnas används källan (eller "senaste" om käll märke också utelämnas).</span><span class="sxs-lookup"><span data-stu-id="3f5d6-146">When tag is omitted the source will be used (or 'latest' if source tag is also omitted).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5d6-147">-UntaggedTargetRepository</span><span class="sxs-lookup"><span data-stu-id="3f5d6-147">-UntaggedTargetRepository</span></span>
<span data-ttu-id="3f5d6-148">Lista över strängar för databas namn för att endast kopiera en manifest kopia.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-148">List of strings of repository names to do a manifest only copy.</span></span>
<span data-ttu-id="3f5d6-149">Ingen tagg skapas.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-149">No tag will be created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5d6-150">-Username</span><span class="sxs-lookup"><span data-stu-id="3f5d6-150">-Username</span></span>
<span data-ttu-id="3f5d6-151">Användar namnet som autentiseras med käll registret.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-151">The username to authenticate with the source registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5d6-152">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3f5d6-152">-Confirm</span></span>
<span data-ttu-id="3f5d6-153">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5d6-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f5d6-154">-WhatIf</span></span>
<span data-ttu-id="3f5d6-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f5d6-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-156">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5d6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f5d6-157">CommonParameters</span></span>
<span data-ttu-id="3f5d6-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f5d6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f5d6-159">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f5d6-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f5d6-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f5d6-160">INPUTS</span></span>

### <span data-ttu-id="3f5d6-161">System. String</span><span class="sxs-lookup"><span data-stu-id="3f5d6-161">System.String</span></span>

## <span data-ttu-id="3f5d6-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f5d6-162">OUTPUTS</span></span>

### <span data-ttu-id="3f5d6-163">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3f5d6-163">System.Boolean</span></span>

## <span data-ttu-id="3f5d6-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f5d6-164">NOTES</span></span>

## <span data-ttu-id="3f5d6-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f5d6-165">RELATED LINKS</span></span>