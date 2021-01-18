---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
ms.openlocfilehash: 162071e07e8081f80e4187f049aef8931dcffc78
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523719"
---
# <span data-ttu-id="fe6f1-101">New-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="fe6f1-101">New-AzWvdMsixPackage</span></span>

## <span data-ttu-id="fe6f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe6f1-102">SYNOPSIS</span></span>
<span data-ttu-id="fe6f1-103">Skapa eller uppdatera ett MSIX-paket.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-103">Create or update a MSIX package.</span></span>

## <span data-ttu-id="fe6f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe6f1-104">SYNTAX</span></span>

### <span data-ttu-id="fe6f1-105">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="fe6f1-105">CreateExpanded (Default)</span></span>
```
New-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-LastUpdated <DateTime>] [-PackageApplication <IMsixPackageApplications[]>]
 [-PackageDependency <IMsixPackageDependencies[]>] [-PackageFamilyName <String>] [-PackageName <String>]
 [-PackageRelativePath <String>] [-Version <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="fe6f1-106">PackageAlias</span><span class="sxs-lookup"><span data-stu-id="fe6f1-106">PackageAlias</span></span>
```
New-AzWvdMsixPackage -HostPoolName <String> -PackageAlias <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="fe6f1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe6f1-107">DESCRIPTION</span></span>
<span data-ttu-id="fe6f1-108">Skapa eller uppdatera ett MSIX-paket.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-108">Create or update a MSIX package.</span></span>

## <span data-ttu-id="fe6f1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe6f1-109">EXAMPLES</span></span>

### <span data-ttu-id="fe6f1-110">Exempel 1: skapar ett nytt MSIX-paket i HostPool-paketets alias</span><span class="sxs-lookup"><span data-stu-id="fe6f1-110">Example 1: Creates New MSIX Package in the HostPool via Package Alias</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
      -PackageAlias packagealias `
      -ImagePath ImagePathURI  `
```

<span data-ttu-id="fe6f1-111">Det här kommandot lägger till MSIX-paketet från angiven bild Sök väg till HostPool</span><span class="sxs-lookup"><span data-stu-id="fe6f1-111">This command adds MSIX package from specified image path to HostPool</span></span>

### <span data-ttu-id="fe6f1-112">Exempel 2: skapar ett nytt MSIX-paket i HostPool</span><span class="sxs-lookup"><span data-stu-id="fe6f1-112">Example 2: Creates New MSIX Package in the HostPool</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -FullName PackageFullName `
                            -HostPoolName HostPoolName `
                            -ResourceGroupName ResourceGroupName ` 
                            -SubscriptionId SubscriptionId ` 
                            -DisplayName displayname `
                            -ImagePath imageURI ` 
                            -IsActive:$false `
                            -IsRegularRegistration:$false `
                            -LastUpdated datelastupdated `
                            -PackageApplication $apps `
                            -PackageDependency $deps `
                            -PackageFamilyName packagefamilyname `
                            -PackageName packagename `
                            -PackageRelativePath packagerelativepath `
                            -Version packageversion `

Name                              Type
----                              ----
HotPoolName/PackageFullName      Microsoft.DesktopVirtualization/hostpools/msixpackages

```

<span data-ttu-id="fe6f1-113">Det här kommandot lägger till MSIX-paketet i angiven HostPool</span><span class="sxs-lookup"><span data-stu-id="fe6f1-113">This command adds MSIX Package in the specified HostPool</span></span>

## <span data-ttu-id="fe6f1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe6f1-114">PARAMETERS</span></span>

### <span data-ttu-id="fe6f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe6f1-115">-DefaultProfile</span></span>
<span data-ttu-id="fe6f1-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6f1-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fe6f1-117">-DisplayName</span></span>
<span data-ttu-id="fe6f1-118">Eget namn som ska visas i portalen.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-118">User friendly Name to be displayed in the portal.</span></span>

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

### <span data-ttu-id="fe6f1-119">-FullName</span><span class="sxs-lookup"><span data-stu-id="fe6f1-119">-FullName</span></span>
<span data-ttu-id="fe6f1-120">Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="fe6f1-120">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6f1-121">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="fe6f1-121">-HostPoolName</span></span>
<span data-ttu-id="fe6f1-122">Namnet på den värdbaserade adresspoolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="fe6f1-122">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="fe6f1-123">-ImagePath</span><span class="sxs-lookup"><span data-stu-id="fe6f1-123">-ImagePath</span></span>
<span data-ttu-id="fe6f1-124">VHD/CIM-avbildningsfil på nätverks resursen.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-124">VHD/CIM image path on Network Share.</span></span>

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

### <span data-ttu-id="fe6f1-125">-IsActive</span><span class="sxs-lookup"><span data-stu-id="fe6f1-125">-IsActive</span></span>
<span data-ttu-id="fe6f1-126">Gör den här versionen av paketet aktiva i hostpool.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-126">Make this version of the package the active one across the hostpool.</span></span>

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

### <span data-ttu-id="fe6f1-127">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="fe6f1-127">-IsRegularRegistration</span></span>
<span data-ttu-id="fe6f1-128">Anger hur du registrerar paket i feed.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-128">Specifies how to register Package in feed.</span></span>

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

### <span data-ttu-id="fe6f1-129">-LastUpdated</span><span class="sxs-lookup"><span data-stu-id="fe6f1-129">-LastUpdated</span></span>
<span data-ttu-id="fe6f1-130">Datum paketet uppdaterades senast, hittades i appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-130">Date Package was last updated, found in the appxmanifest.xml.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6f1-131">-PackageAlias</span><span class="sxs-lookup"><span data-stu-id="fe6f1-131">-PackageAlias</span></span>
<span data-ttu-id="fe6f1-132">Paket Ali Aset från extrahera MSIX-bild</span><span class="sxs-lookup"><span data-stu-id="fe6f1-132">Package Alias from extract MSIX Image</span></span>

```yaml
Type: System.String
Parameter Sets: PackageAlias
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6f1-133">-PackageApplication</span><span class="sxs-lookup"><span data-stu-id="fe6f1-133">-PackageApplication</span></span>
<span data-ttu-id="fe6f1-134">Lista över paket program.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-134">List of package applications.</span></span>

<span data-ttu-id="fe6f1-135">För att konstruera kan du läsa avsnittet anteckningar för PACKAGEAPPLICATION-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-135">To construct, see NOTES section for PACKAGEAPPLICATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackageApplications[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6f1-136">-PackageDependency</span><span class="sxs-lookup"><span data-stu-id="fe6f1-136">-PackageDependency</span></span>
<span data-ttu-id="fe6f1-137">Lista med paket beroenden.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-137">List of package dependencies.</span></span>

<span data-ttu-id="fe6f1-138">För att konstruera kan du läsa avsnittet anteckningar för PACKAGEDEPENDENCY-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-138">To construct, see NOTES section for PACKAGEDEPENDENCY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackageDependencies[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6f1-139">-PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="fe6f1-139">-PackageFamilyName</span></span>
<span data-ttu-id="fe6f1-140">Paket familje namn från appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-140">Package Family Name from appxmanifest.xml.</span></span>
<span data-ttu-id="fe6f1-141">Innehåller paket namn och utgivarens namn.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-141">Contains Package Name and Publisher name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6f1-142">-PackageName</span><span class="sxs-lookup"><span data-stu-id="fe6f1-142">-PackageName</span></span>
<span data-ttu-id="fe6f1-143">Paket namn från appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-143">Package Name from appxmanifest.xml.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6f1-144">-PackageRelativePath</span><span class="sxs-lookup"><span data-stu-id="fe6f1-144">-PackageRelativePath</span></span>
<span data-ttu-id="fe6f1-145">Relativ sökväg till paketet i bilden.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-145">Relative Path to the package inside the image.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6f1-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe6f1-146">-ResourceGroupName</span></span>
<span data-ttu-id="fe6f1-147">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-147">The name of the resource group.</span></span>
<span data-ttu-id="fe6f1-148">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-148">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fe6f1-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe6f1-149">-SubscriptionId</span></span>
<span data-ttu-id="fe6f1-150">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-150">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6f1-151">-Version</span><span class="sxs-lookup"><span data-stu-id="fe6f1-151">-Version</span></span>
<span data-ttu-id="fe6f1-152">Paket version finns i appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-152">Package Version found in the appxmanifest.xml.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6f1-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fe6f1-153">-Confirm</span></span>
<span data-ttu-id="fe6f1-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe6f1-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe6f1-155">-WhatIf</span></span>
<span data-ttu-id="fe6f1-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe6f1-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe6f1-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe6f1-158">CommonParameters</span></span>
<span data-ttu-id="fe6f1-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe6f1-160">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe6f1-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe6f1-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe6f1-161">INPUTS</span></span>

## <span data-ttu-id="fe6f1-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe6f1-162">OUTPUTS</span></span>

### <span data-ttu-id="fe6f1-163">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20201102Preview. IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="fe6f1-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="fe6f1-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe6f1-164">NOTES</span></span>

<span data-ttu-id="fe6f1-165">ALIAS</span><span class="sxs-lookup"><span data-stu-id="fe6f1-165">ALIASES</span></span>

<span data-ttu-id="fe6f1-166">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="fe6f1-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fe6f1-167">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fe6f1-168">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fe6f1-169">PACKAGEAPPLICATION <IMsixPackageApplications [] >: lista med paket program.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: List of package applications.</span></span> 
  - <span data-ttu-id="fe6f1-170">`[AppId <String>]`: Program-ID för paket, som finns i appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-170">`[AppId <String>]`: Package Application Id, found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="fe6f1-171">`[AppUserModelId <String>]`: Används för att aktivera paket programmet.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-171">`[AppUserModelId <String>]`: Used to activate Package Application.</span></span> <span data-ttu-id="fe6f1-172">Består av paket namn och ApplicationID.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-172">Consists of Package Name and ApplicationID.</span></span> <span data-ttu-id="fe6f1-173">Finns i appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-173">Found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="fe6f1-174">`[Description <String>]`: Beskrivning av program för paket.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-174">`[Description <String>]`: Description of Package Application.</span></span>
  - <span data-ttu-id="fe6f1-175">`[FriendlyName <String>]`: Eget namn på användare.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-175">`[FriendlyName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="fe6f1-176">`[IconImageName <String>]`: Eget namn på användare.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-176">`[IconImageName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="fe6f1-177">`[RawIcon <Byte[]>]`: ikonen en 64-bit-sträng som en byte-matris.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-177">`[RawIcon <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>
  - <span data-ttu-id="fe6f1-178">`[RawPng <Byte[]>]`: ikonen en 64-bit-sträng som en byte-matris.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-178">`[RawPng <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>

<span data-ttu-id="fe6f1-179">PACKAGEDEPENDENCY <IMsixPackageDependencies [] >: lista med paket beroenden.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: List of package dependencies.</span></span> 
  - <span data-ttu-id="fe6f1-180">`[DependencyName <String>]`: Namnet på paket beroendet.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-180">`[DependencyName <String>]`: Name of package dependency.</span></span>
  - <span data-ttu-id="fe6f1-181">`[MinVersion <String>]`: Beroende version krävs.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-181">`[MinVersion <String>]`: Dependency version required.</span></span>
  - <span data-ttu-id="fe6f1-182">`[Publisher <String>]`: Beroende utgivarens namn.</span><span class="sxs-lookup"><span data-stu-id="fe6f1-182">`[Publisher <String>]`: Name of dependency publisher.</span></span>

## <span data-ttu-id="fe6f1-183">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe6f1-183">RELATED LINKS</span></span>

