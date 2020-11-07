---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
ms.openlocfilehash: 7a337ed6e347d5ab22cd04baac2acb1c7e0b171d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919930"
---
# <span data-ttu-id="bd722-101">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="bd722-101">New-AzServiceFabricApplication</span></span>

## <span data-ttu-id="bd722-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd722-102">SYNOPSIS</span></span>
<span data-ttu-id="bd722-103">Skapa ett nytt tjänst Fabric-program under den angivna resurs gruppen och klustret.</span><span class="sxs-lookup"><span data-stu-id="bd722-103">Create new service fabric application under the specified resource group and cluster.</span></span>

## <span data-ttu-id="bd722-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd722-104">SYNTAX</span></span>

### <span data-ttu-id="bd722-105">SkipAppTypeVersion (standard)</span><span class="sxs-lookup"><span data-stu-id="bd722-105">SkipAppTypeVersion (Default)</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd722-106">CreateAppTypeVersion</span><span class="sxs-lookup"><span data-stu-id="bd722-106">CreateAppTypeVersion</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] -PackageUrl <String> [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd722-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd722-107">DESCRIPTION</span></span>
<span data-ttu-id="bd722-108">Denna cmdlet skapar ett nytt tjänst Fabric-program under den angivna resurs gruppen och klustret.</span><span class="sxs-lookup"><span data-stu-id="bd722-108">This cmdlet creates a new service fabric application under the specified resource group and cluster.</span></span> <span data-ttu-id="bd722-109">Parametern-PackageUrl kan användas för att skapa typ versionen, om typ versionen redan har avslut ATS men dess i tillståndet ' Failed ' frågar cmdleten om användaren vill återskapa typ versionen.</span><span class="sxs-lookup"><span data-stu-id="bd722-109">The parameter -PackageUrl can be used to create the type version, If the type version already exits but its in 'Failed' state the cmdlet will ask if the user wants to recreate the type version.</span></span> <span data-ttu-id="bd722-110">Om det fortsätter i tillståndet ' Failed ' stoppar kommandot processen och returnerar ett undantag.</span><span class="sxs-lookup"><span data-stu-id="bd722-110">If it continues in 'Failed' state, the command will stop the process and throw an exception.</span></span>

## <span data-ttu-id="bd722-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd722-111">EXAMPLES</span></span>

### <span data-ttu-id="bd722-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bd722-112">Example 1</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="bd722-113">I det här exemplet skapas programmet "testApp" under resurs gruppen "testRG" och cluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="bd722-113">This example creates the application "testApp" under resource group "testRG" and cluster "testCluster".</span></span> <span data-ttu-id="bd722-114">Program typen "TestAppType" version "v1" bör redan finnas i klustret, och tillämpnings parametrarna bör definieras i program manifestet annars Miss lyckas cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bd722-114">The application type "TestAppType" version "v1" should already exist in the cluster, and the application parameters should be defined in the application manifest otherwise the cmdlet will fail.</span></span>

### <span data-ttu-id="bd722-115">Exempel 2: Ange-PackageUrl för att skapa program typs versionen innan du skapar programmet.</span><span class="sxs-lookup"><span data-stu-id="bd722-115">Example 2: Specify -PackageUrl to create the application type version before creating the application.</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -PackageUrl "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="bd722-116">I det här exemplet skapas program typen "TestAppType" version "v1" med den angivna paket-URL: en.</span><span class="sxs-lookup"><span data-stu-id="bd722-116">This example creates the application type "TestAppType"  version "v1" using the package url provided.</span></span> <span data-ttu-id="bd722-117">Därefter fortsätter den vanliga processen att skapa programmet.</span><span class="sxs-lookup"><span data-stu-id="bd722-117">After this, it will continue the normal process to create the application.</span></span> <span data-ttu-id="bd722-118">Om program typs versionen redan har avslut ATS och etablerings statusen i ' misslyckades ', uppmanas du att avgöra om användaren vill återskapa typ versionen.</span><span class="sxs-lookup"><span data-stu-id="bd722-118">If the application type version already exits and the provisioning state its in 'Failed' it will prompt to decide if the user wants to recreate the type version.</span></span>

## <span data-ttu-id="bd722-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd722-119">PARAMETERS</span></span>

### <span data-ttu-id="bd722-120">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="bd722-120">-ApplicationParameter</span></span>
<span data-ttu-id="bd722-121">Ange program parametrar som nycklar/värde par.</span><span class="sxs-lookup"><span data-stu-id="bd722-121">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="bd722-122">Dessa parametrar måste finnas i program manifestet.</span><span class="sxs-lookup"><span data-stu-id="bd722-122">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="bd722-123">-ApplicationTypeName</span><span class="sxs-lookup"><span data-stu-id="bd722-123">-ApplicationTypeName</span></span>
<span data-ttu-id="bd722-124">Ange namnet på program typen</span><span class="sxs-lookup"><span data-stu-id="bd722-124">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd722-125">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="bd722-125">-ApplicationTypeVersion</span></span>
<span data-ttu-id="bd722-126">Ange program typ version</span><span class="sxs-lookup"><span data-stu-id="bd722-126">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd722-127">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="bd722-127">-ClusterName</span></span>
<span data-ttu-id="bd722-128">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="bd722-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="bd722-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd722-129">-DefaultProfile</span></span>
<span data-ttu-id="bd722-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd722-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd722-131">-Force</span><span class="sxs-lookup"><span data-stu-id="bd722-131">-Force</span></span>
<span data-ttu-id="bd722-132">Fortsätt utan uppmaningar</span><span class="sxs-lookup"><span data-stu-id="bd722-132">Continue without prompts</span></span>

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

### <span data-ttu-id="bd722-133">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="bd722-133">-MaximumNodeCount</span></span>
<span data-ttu-id="bd722-134">Anger det högsta antalet noder som ett program ska placeras på</span><span class="sxs-lookup"><span data-stu-id="bd722-134">Specifies the maximum number of nodes on which to place an application</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd722-135">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="bd722-135">-MinimumNodeCount</span></span>
<span data-ttu-id="bd722-136">Anger det minsta antalet noder där tjänste infrastruktur ska reservera kapacitet för det här programmet</span><span class="sxs-lookup"><span data-stu-id="bd722-136">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd722-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="bd722-137">-Name</span></span>
<span data-ttu-id="bd722-138">Ange namnet på programmet</span><span class="sxs-lookup"><span data-stu-id="bd722-138">Specify the name of the application</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd722-139">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="bd722-139">-PackageUrl</span></span>
<span data-ttu-id="bd722-140">Ange URL-adressen för programpaketets sfpkg-fil</span><span class="sxs-lookup"><span data-stu-id="bd722-140">Specify the url of the application package sfpkg file</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAppTypeVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd722-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd722-141">-ResourceGroupName</span></span>
<span data-ttu-id="bd722-142">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bd722-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="bd722-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bd722-143">-Confirm</span></span>
<span data-ttu-id="bd722-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bd722-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd722-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd722-145">-WhatIf</span></span>
<span data-ttu-id="bd722-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bd722-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd722-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bd722-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd722-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd722-148">CommonParameters</span></span>
<span data-ttu-id="bd722-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd722-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd722-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd722-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd722-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd722-151">INPUTS</span></span>

### <span data-ttu-id="bd722-152">System. String</span><span class="sxs-lookup"><span data-stu-id="bd722-152">System.String</span></span>

### <span data-ttu-id="bd722-153">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="bd722-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bd722-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd722-154">OUTPUTS</span></span>

### <span data-ttu-id="bd722-155">Microsoft. Azure. commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="bd722-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="bd722-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd722-156">NOTES</span></span>

## <span data-ttu-id="bd722-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd722-157">RELATED LINKS</span></span>
