---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
ms.openlocfilehash: 5295caae4ffa0138a1c81fd08a5614f6e636eb41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101955"
---
# <span data-ttu-id="e924a-101">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e924a-101">New-AzServiceFabricApplication</span></span>

## <span data-ttu-id="e924a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e924a-102">SYNOPSIS</span></span>
<span data-ttu-id="e924a-103">Skapa ett nytt tjänst Fabric-program under den angivna resurs gruppen och klustret.</span><span class="sxs-lookup"><span data-stu-id="e924a-103">Create new service fabric application under the specified resource group and cluster.</span></span>

## <span data-ttu-id="e924a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e924a-104">SYNTAX</span></span>

### <span data-ttu-id="e924a-105">SkipAppTypeVersion (standard)</span><span class="sxs-lookup"><span data-stu-id="e924a-105">SkipAppTypeVersion (Default)</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e924a-106">CreateAppTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e924a-106">CreateAppTypeVersion</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] -PackageUrl <String> [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e924a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e924a-107">DESCRIPTION</span></span>
<span data-ttu-id="e924a-108">Denna cmdlet skapar ett nytt tjänst Fabric-program under den angivna resurs gruppen och klustret.</span><span class="sxs-lookup"><span data-stu-id="e924a-108">This cmdlet creates a new service fabric application under the specified resource group and cluster.</span></span> <span data-ttu-id="e924a-109">Parametern-PackageUrl kan användas för att skapa typ versionen, om typ versionen redan har avslut ATS men dess i tillståndet ' Failed ' frågar cmdleten om användaren vill återskapa typ versionen.</span><span class="sxs-lookup"><span data-stu-id="e924a-109">The parameter -PackageUrl can be used to create the type version, If the type version already exits but its in 'Failed' state the cmdlet will ask if the user wants to recreate the type version.</span></span> <span data-ttu-id="e924a-110">Om det fortsätter i tillståndet ' Failed ' stoppar kommandot processen och returnerar ett undantag.</span><span class="sxs-lookup"><span data-stu-id="e924a-110">If it continues in 'Failed' state, the command will stop the process and throw an exception.</span></span>

## <span data-ttu-id="e924a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e924a-111">EXAMPLES</span></span>

### <span data-ttu-id="e924a-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e924a-112">Example 1</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="e924a-113">I det här exemplet skapas programmet "testApp" under resurs gruppen "testRG" och cluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="e924a-113">This example creates the application "testApp" under resource group "testRG" and cluster "testCluster".</span></span> <span data-ttu-id="e924a-114">Program typen "TestAppType" version "v1" bör redan finnas i klustret, och tillämpnings parametrarna bör definieras i program manifestet annars Miss lyckas cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e924a-114">The application type "TestAppType" version "v1" should already exist in the cluster, and the application parameters should be defined in the application manifest otherwise the cmdlet will fail.</span></span>

### <span data-ttu-id="e924a-115">Exempel 2: Ange-PackageUrl för att skapa program typs versionen innan du skapar programmet.</span><span class="sxs-lookup"><span data-stu-id="e924a-115">Example 2: Specify -PackageUrl to create the application type version before creating the application.</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -PackageUrl "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="e924a-116">I det här exemplet skapas program typen "TestAppType" version "v1" med den angivna paket-URL: en.</span><span class="sxs-lookup"><span data-stu-id="e924a-116">This example creates the application type "TestAppType"  version "v1" using the package url provided.</span></span> <span data-ttu-id="e924a-117">Därefter fortsätter den vanliga processen att skapa programmet.</span><span class="sxs-lookup"><span data-stu-id="e924a-117">After this, it will continue the normal process to create the application.</span></span> <span data-ttu-id="e924a-118">Om program typs versionen redan har avslut ATS och etablerings statusen i ' misslyckades ', uppmanas du att avgöra om användaren vill återskapa typ versionen.</span><span class="sxs-lookup"><span data-stu-id="e924a-118">If the application type version already exits and the provisioning state its in 'Failed' it will prompt to decide if the user wants to recreate the type version.</span></span>

## <span data-ttu-id="e924a-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e924a-119">PARAMETERS</span></span>

### <span data-ttu-id="e924a-120">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="e924a-120">-ApplicationParameter</span></span>
<span data-ttu-id="e924a-121">Ange program parametrar som nycklar/värde par.</span><span class="sxs-lookup"><span data-stu-id="e924a-121">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="e924a-122">Dessa parametrar måste finnas i program manifestet.</span><span class="sxs-lookup"><span data-stu-id="e924a-122">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="e924a-123">-ApplicationTypeName</span><span class="sxs-lookup"><span data-stu-id="e924a-123">-ApplicationTypeName</span></span>
<span data-ttu-id="e924a-124">Ange namnet på program typen</span><span class="sxs-lookup"><span data-stu-id="e924a-124">Specify the name of the application type</span></span>

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

### <span data-ttu-id="e924a-125">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e924a-125">-ApplicationTypeVersion</span></span>
<span data-ttu-id="e924a-126">Ange program typ version</span><span class="sxs-lookup"><span data-stu-id="e924a-126">Specify the application type version</span></span>

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

### <span data-ttu-id="e924a-127">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="e924a-127">-ClusterName</span></span>
<span data-ttu-id="e924a-128">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="e924a-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e924a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e924a-129">-DefaultProfile</span></span>
<span data-ttu-id="e924a-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e924a-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e924a-131">-Force</span><span class="sxs-lookup"><span data-stu-id="e924a-131">-Force</span></span>
<span data-ttu-id="e924a-132">Fortsätt utan uppmaningar</span><span class="sxs-lookup"><span data-stu-id="e924a-132">Continue without prompts</span></span>

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

### <span data-ttu-id="e924a-133">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="e924a-133">-MaximumNodeCount</span></span>
<span data-ttu-id="e924a-134">Anger det högsta antalet noder som ett program ska placeras på</span><span class="sxs-lookup"><span data-stu-id="e924a-134">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="e924a-135">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="e924a-135">-MinimumNodeCount</span></span>
<span data-ttu-id="e924a-136">Anger det minsta antalet noder där tjänste infrastruktur ska reservera kapacitet för det här programmet</span><span class="sxs-lookup"><span data-stu-id="e924a-136">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="e924a-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="e924a-137">-Name</span></span>
<span data-ttu-id="e924a-138">Ange namnet på programmet</span><span class="sxs-lookup"><span data-stu-id="e924a-138">Specify the name of the application</span></span>

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

### <span data-ttu-id="e924a-139">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="e924a-139">-PackageUrl</span></span>
<span data-ttu-id="e924a-140">Ange URL-adressen för programpaketets sfpkg-fil</span><span class="sxs-lookup"><span data-stu-id="e924a-140">Specify the url of the application package sfpkg file</span></span>

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

### <span data-ttu-id="e924a-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e924a-141">-ResourceGroupName</span></span>
<span data-ttu-id="e924a-142">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e924a-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e924a-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e924a-143">-Confirm</span></span>
<span data-ttu-id="e924a-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e924a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e924a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e924a-145">-WhatIf</span></span>
<span data-ttu-id="e924a-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e924a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e924a-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e924a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e924a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e924a-148">CommonParameters</span></span>
<span data-ttu-id="e924a-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e924a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e924a-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e924a-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e924a-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e924a-151">INPUTS</span></span>

### <span data-ttu-id="e924a-152">System. String</span><span class="sxs-lookup"><span data-stu-id="e924a-152">System.String</span></span>

### <span data-ttu-id="e924a-153">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="e924a-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e924a-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e924a-154">OUTPUTS</span></span>

### <span data-ttu-id="e924a-155">Microsoft. Azure. commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="e924a-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="e924a-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e924a-156">NOTES</span></span>

## <span data-ttu-id="e924a-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e924a-157">RELATED LINKS</span></span>
