---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
ms.openlocfilehash: fd5dd920863d4bd53257cfe2170e83f53c620096
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409416"
---
# <span data-ttu-id="49bc5-101">New-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="49bc5-101">New-AzWvdMsixPackage</span></span>

## <span data-ttu-id="49bc5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="49bc5-103">Skapa eller uppdatera ett MSIX-paket.</span><span class="sxs-lookup"><span data-stu-id="49bc5-103">Create or update a MSIX package.</span></span>

## <span data-ttu-id="49bc5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49bc5-104">SYNTAX</span></span>

### <span data-ttu-id="49bc5-105">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="49bc5-105">CreateExpanded (Default)</span></span>
```
New-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-LastUpdated <DateTime>] [-PackageApplication <IMsixPackageApplications[]>]
 [-PackageDependency <IMsixPackageDependencies[]>] [-PackageFamilyName <String>] [-PackageName <String>]
 [-PackageRelativePath <String>] [-Version <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="49bc5-106">PackageAlias</span><span class="sxs-lookup"><span data-stu-id="49bc5-106">PackageAlias</span></span>
```
New-AzWvdMsixPackage -HostPoolName <String> -PackageAlias <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="49bc5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49bc5-107">DESCRIPTION</span></span>
<span data-ttu-id="49bc5-108">Skapa eller uppdatera ett MSIX-paket.</span><span class="sxs-lookup"><span data-stu-id="49bc5-108">Create or update a MSIX package.</span></span>

## <span data-ttu-id="49bc5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49bc5-109">EXAMPLES</span></span>

### <span data-ttu-id="49bc5-110">Exempel 1: skapar ett nytt MSIX-paket i HostPool-paketets alias</span><span class="sxs-lookup"><span data-stu-id="49bc5-110">Example 1: Creates New MSIX Package in the HostPool via Package Alias</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
      -PackageAlias packagealias `
      -ImagePath ImagePathURI  `
```

<span data-ttu-id="49bc5-111">Det här kommandot lägger till MSIX-paketet från angiven bild Sök väg till HostPool</span><span class="sxs-lookup"><span data-stu-id="49bc5-111">This command adds MSIX package from specified image path to HostPool</span></span>

### <span data-ttu-id="49bc5-112">Exempel 2: skapar ett nytt MSIX-paket i HostPool</span><span class="sxs-lookup"><span data-stu-id="49bc5-112">Example 2: Creates New MSIX Package in the HostPool</span></span>
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

<span data-ttu-id="49bc5-113">Det här kommandot lägger till MSIX-paketet i angiven HostPool</span><span class="sxs-lookup"><span data-stu-id="49bc5-113">This command adds MSIX Package in the specified HostPool</span></span>

## <span data-ttu-id="49bc5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49bc5-114">PARAMETERS</span></span>

### <span data-ttu-id="49bc5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49bc5-115">-DefaultProfile</span></span>
<span data-ttu-id="49bc5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="49bc5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49bc5-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="49bc5-117">-DisplayName</span></span>
<span data-ttu-id="49bc5-118">Eget namn som ska visas i portalen.</span><span class="sxs-lookup"><span data-stu-id="49bc5-118">User friendly Name to be displayed in the portal.</span></span>

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

### <span data-ttu-id="49bc5-119">-FullName</span><span class="sxs-lookup"><span data-stu-id="49bc5-119">-FullName</span></span>
<span data-ttu-id="49bc5-120">Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool</span><span class="sxs-lookup"><span data-stu-id="49bc5-120">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="49bc5-121">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="49bc5-121">-HostPoolName</span></span>
<span data-ttu-id="49bc5-122">Namnet på den värdbaserade adresspoolen i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="49bc5-122">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="49bc5-123">-ImagePath</span><span class="sxs-lookup"><span data-stu-id="49bc5-123">-ImagePath</span></span>
<span data-ttu-id="49bc5-124">VHD/CIM-avbildningsfil på nätverks resursen.</span><span class="sxs-lookup"><span data-stu-id="49bc5-124">VHD/CIM image path on Network Share.</span></span>

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

### <span data-ttu-id="49bc5-125">-IsActive</span><span class="sxs-lookup"><span data-stu-id="49bc5-125">-IsActive</span></span>
<span data-ttu-id="49bc5-126">Gör den här versionen av paketet aktiva i hostpool.</span><span class="sxs-lookup"><span data-stu-id="49bc5-126">Make this version of the package the active one across the hostpool.</span></span>

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

### <span data-ttu-id="49bc5-127">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="49bc5-127">-IsRegularRegistration</span></span>
<span data-ttu-id="49bc5-128">Anger hur du registrerar paket i feed.</span><span class="sxs-lookup"><span data-stu-id="49bc5-128">Specifies how to register Package in feed.</span></span>

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

### <span data-ttu-id="49bc5-129">-LastUpdated</span><span class="sxs-lookup"><span data-stu-id="49bc5-129">-LastUpdated</span></span>
<span data-ttu-id="49bc5-130">Datum paketet uppdaterades senast, hittades i appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="49bc5-130">Date Package was last updated, found in the appxmanifest.xml.</span></span>

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

### <span data-ttu-id="49bc5-131">-PackageAlias</span><span class="sxs-lookup"><span data-stu-id="49bc5-131">-PackageAlias</span></span>
<span data-ttu-id="49bc5-132">Paket Ali Aset från extrahera MSIX-bild</span><span class="sxs-lookup"><span data-stu-id="49bc5-132">Package Alias from extract MSIX Image</span></span>

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

### <span data-ttu-id="49bc5-133">-PackageApplication</span><span class="sxs-lookup"><span data-stu-id="49bc5-133">-PackageApplication</span></span>
<span data-ttu-id="49bc5-134">Lista över paket program.</span><span class="sxs-lookup"><span data-stu-id="49bc5-134">List of package applications.</span></span>

<span data-ttu-id="49bc5-135">För att konstruera kan du läsa avsnittet anteckningar för PACKAGEAPPLICATION-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="49bc5-135">To construct, see NOTES section for PACKAGEAPPLICATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackageApplications[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49bc5-136">-PackageDependency</span><span class="sxs-lookup"><span data-stu-id="49bc5-136">-PackageDependency</span></span>
<span data-ttu-id="49bc5-137">Lista med paket beroenden.</span><span class="sxs-lookup"><span data-stu-id="49bc5-137">List of package dependencies.</span></span>

<span data-ttu-id="49bc5-138">För att konstruera kan du läsa avsnittet anteckningar för PACKAGEDEPENDENCY-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="49bc5-138">To construct, see NOTES section for PACKAGEDEPENDENCY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackageDependencies[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49bc5-139">-PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="49bc5-139">-PackageFamilyName</span></span>
<span data-ttu-id="49bc5-140">Paket familje namn från appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="49bc5-140">Package Family Name from appxmanifest.xml.</span></span>
<span data-ttu-id="49bc5-141">Innehåller paket namn och utgivarens namn.</span><span class="sxs-lookup"><span data-stu-id="49bc5-141">Contains Package Name and Publisher name.</span></span>

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

### <span data-ttu-id="49bc5-142">-PackageName</span><span class="sxs-lookup"><span data-stu-id="49bc5-142">-PackageName</span></span>
<span data-ttu-id="49bc5-143">Paket namn från appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="49bc5-143">Package Name from appxmanifest.xml.</span></span>

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

### <span data-ttu-id="49bc5-144">-PackageRelativePath</span><span class="sxs-lookup"><span data-stu-id="49bc5-144">-PackageRelativePath</span></span>
<span data-ttu-id="49bc5-145">Relativ sökväg till paketet i bilden.</span><span class="sxs-lookup"><span data-stu-id="49bc5-145">Relative Path to the package inside the image.</span></span>

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

### <span data-ttu-id="49bc5-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49bc5-146">-ResourceGroupName</span></span>
<span data-ttu-id="49bc5-147">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="49bc5-147">The name of the resource group.</span></span>
<span data-ttu-id="49bc5-148">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="49bc5-148">The name is case insensitive.</span></span>

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

### <span data-ttu-id="49bc5-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49bc5-149">-SubscriptionId</span></span>
<span data-ttu-id="49bc5-150">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="49bc5-150">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="49bc5-151">-Version</span><span class="sxs-lookup"><span data-stu-id="49bc5-151">-Version</span></span>
<span data-ttu-id="49bc5-152">Paket version finns i appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="49bc5-152">Package Version found in the appxmanifest.xml.</span></span>

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

### <span data-ttu-id="49bc5-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="49bc5-153">-Confirm</span></span>
<span data-ttu-id="49bc5-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="49bc5-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49bc5-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49bc5-155">-WhatIf</span></span>
<span data-ttu-id="49bc5-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="49bc5-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49bc5-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="49bc5-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49bc5-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49bc5-158">CommonParameters</span></span>
<span data-ttu-id="49bc5-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49bc5-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49bc5-160">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49bc5-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49bc5-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49bc5-161">INPUTS</span></span>

## <span data-ttu-id="49bc5-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49bc5-162">OUTPUTS</span></span>

### <span data-ttu-id="49bc5-163">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20201019Preview. IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="49bc5-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span></span>

## <span data-ttu-id="49bc5-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49bc5-164">NOTES</span></span>

<span data-ttu-id="49bc5-165">ALIAS</span><span class="sxs-lookup"><span data-stu-id="49bc5-165">ALIASES</span></span>

<span data-ttu-id="49bc5-166">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="49bc5-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="49bc5-167">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="49bc5-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="49bc5-168">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="49bc5-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="49bc5-169">PACKAGEAPPLICATION <IMsixPackageApplications [] >: lista med paket program.</span><span class="sxs-lookup"><span data-stu-id="49bc5-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: List of package applications.</span></span> 
  - <span data-ttu-id="49bc5-170">`[AppId <String>]`: Program-ID för paket, som finns i appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="49bc5-170">`[AppId <String>]`: Package Application Id, found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="49bc5-171">`[AppUserModelId <String>]`: Används för att aktivera paket programmet.</span><span class="sxs-lookup"><span data-stu-id="49bc5-171">`[AppUserModelId <String>]`: Used to activate Package Application.</span></span> <span data-ttu-id="49bc5-172">Består av paket namn och ApplicationID.</span><span class="sxs-lookup"><span data-stu-id="49bc5-172">Consists of Package Name and ApplicationID.</span></span> <span data-ttu-id="49bc5-173">Finns i appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="49bc5-173">Found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="49bc5-174">`[Description <String>]`: Beskrivning av program för paket.</span><span class="sxs-lookup"><span data-stu-id="49bc5-174">`[Description <String>]`: Description of Package Application.</span></span>
  - <span data-ttu-id="49bc5-175">`[FriendlyName <String>]`: Eget namn på användare.</span><span class="sxs-lookup"><span data-stu-id="49bc5-175">`[FriendlyName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="49bc5-176">`[IconImageName <String>]`: Eget namn på användare.</span><span class="sxs-lookup"><span data-stu-id="49bc5-176">`[IconImageName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="49bc5-177">`[RawIcon <Byte[]>]`: ikonen en 64-bit-sträng som en byte-matris.</span><span class="sxs-lookup"><span data-stu-id="49bc5-177">`[RawIcon <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>
  - <span data-ttu-id="49bc5-178">`[RawPng <Byte[]>]`: ikonen en 64-bit-sträng som en byte-matris.</span><span class="sxs-lookup"><span data-stu-id="49bc5-178">`[RawPng <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>

<span data-ttu-id="49bc5-179">PACKAGEDEPENDENCY <IMsixPackageDependencies [] >: lista med paket beroenden.</span><span class="sxs-lookup"><span data-stu-id="49bc5-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: List of package dependencies.</span></span> 
  - <span data-ttu-id="49bc5-180">`[DependencyName <String>]`: Namnet på paket beroendet.</span><span class="sxs-lookup"><span data-stu-id="49bc5-180">`[DependencyName <String>]`: Name of package dependency.</span></span>
  - <span data-ttu-id="49bc5-181">`[MinVersion <String>]`: Beroende version krävs.</span><span class="sxs-lookup"><span data-stu-id="49bc5-181">`[MinVersion <String>]`: Dependency version required.</span></span>
  - <span data-ttu-id="49bc5-182">`[Publisher <String>]`: Beroende utgivarens namn.</span><span class="sxs-lookup"><span data-stu-id="49bc5-182">`[Publisher <String>]`: Name of dependency publisher.</span></span>

## <span data-ttu-id="49bc5-183">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49bc5-183">RELATED LINKS</span></span>

