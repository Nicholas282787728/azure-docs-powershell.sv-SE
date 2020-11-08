---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 69bbcbbd508a5bf32163b91378aab62dbdcb3a64
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089452"
---
# <span data-ttu-id="9324e-101">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="9324e-101">New-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="9324e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9324e-102">SYNOPSIS</span></span>
<span data-ttu-id="9324e-103">Skapa en ny program typs version under den angivna resurs gruppen och klustret.</span><span class="sxs-lookup"><span data-stu-id="9324e-103">Create new application type version under the specified resource group and cluster.</span></span>

## <span data-ttu-id="9324e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9324e-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> -PackageUrl <String> [-DefaultParameter <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9324e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9324e-105">DESCRIPTION</span></span>
<span data-ttu-id="9324e-106">Denna cmdlet skapar en ny program typs version genom att använda paketet som anges i-PackageUrl, det ska vara tillgängligt via en REST-slutpunkt för Azure Resource Manager för användning under distributionen och innehöll programmet paketerat och zippat med fil namns tillägget. sfpkg.</span><span class="sxs-lookup"><span data-stu-id="9324e-106">This cmdlet creates a new application type version using the package specified in -PackageUrl, this should be accessible through a REST endpoint for Azure Resource Manager to consume during deployment and contained The application packaged and zipped with the extension .sfpkg.</span></span> <span data-ttu-id="9324e-107">Det här kommandot skapar program typen om den inte redan finns.</span><span class="sxs-lookup"><span data-stu-id="9324e-107">This command will create the application type if it doesn't exist already.</span></span>

## <span data-ttu-id="9324e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9324e-108">EXAMPLES</span></span>

### <span data-ttu-id="9324e-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9324e-109">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -PackageUrl $packageUrl -Verbose
```

<span data-ttu-id="9324e-110">I det här exemplet skapas en version "v1" under typ "testAppType".</span><span class="sxs-lookup"><span data-stu-id="9324e-110">This example will create an application type version "v1" under type "testAppType".</span></span> <span data-ttu-id="9324e-111">Versionen i program manifestet i paketet ska ha samma version som den som anges i versionen.</span><span class="sxs-lookup"><span data-stu-id="9324e-111">The version in the application manifest contained in the package should have the same version as the one specified in -Version.</span></span>

## <span data-ttu-id="9324e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9324e-112">PARAMETERS</span></span>

### <span data-ttu-id="9324e-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="9324e-113">-ClusterName</span></span>
<span data-ttu-id="9324e-114">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="9324e-114">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9324e-115">-DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="9324e-115">-DefaultParameter</span></span>
<span data-ttu-id="9324e-116">Ange standardvärden för program parametrarna som nycklar/värde-par.</span><span class="sxs-lookup"><span data-stu-id="9324e-116">Specify the default values of the application parameters as key/value pairs.</span></span>
<span data-ttu-id="9324e-117">Dessa parametrar måste finnas i program manifestet.</span><span class="sxs-lookup"><span data-stu-id="9324e-117">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9324e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9324e-118">-DefaultProfile</span></span>
<span data-ttu-id="9324e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9324e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9324e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9324e-120">-Force</span></span>
<span data-ttu-id="9324e-121">Fortsätt utan uppmaningar</span><span class="sxs-lookup"><span data-stu-id="9324e-121">Continue without prompts</span></span>

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

### <span data-ttu-id="9324e-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="9324e-122">-Name</span></span>
<span data-ttu-id="9324e-123">Ange namnet på program typen</span><span class="sxs-lookup"><span data-stu-id="9324e-123">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9324e-124">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="9324e-124">-PackageUrl</span></span>
<span data-ttu-id="9324e-125">Ange URL-adressen för programpaketets sfpkg-fil</span><span class="sxs-lookup"><span data-stu-id="9324e-125">Specify the url of the application package sfpkg file</span></span>

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

### <span data-ttu-id="9324e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9324e-126">-ResourceGroupName</span></span>
<span data-ttu-id="9324e-127">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9324e-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9324e-128">-Version</span><span class="sxs-lookup"><span data-stu-id="9324e-128">-Version</span></span>
<span data-ttu-id="9324e-129">Ange program typ version</span><span class="sxs-lookup"><span data-stu-id="9324e-129">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9324e-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9324e-130">-Confirm</span></span>
<span data-ttu-id="9324e-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9324e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9324e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9324e-132">-WhatIf</span></span>
<span data-ttu-id="9324e-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9324e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9324e-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9324e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9324e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9324e-135">CommonParameters</span></span>
<span data-ttu-id="9324e-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9324e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9324e-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9324e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9324e-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9324e-138">INPUTS</span></span>

### <span data-ttu-id="9324e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9324e-139">System.String</span></span>

### <span data-ttu-id="9324e-140">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="9324e-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9324e-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9324e-141">OUTPUTS</span></span>

### <span data-ttu-id="9324e-142">Microsoft. Azure. commands. ServiceFabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="9324e-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="9324e-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9324e-143">NOTES</span></span>

## <span data-ttu-id="9324e-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9324e-144">RELATED LINKS</span></span>
