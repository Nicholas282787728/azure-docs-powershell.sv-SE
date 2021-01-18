---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 88c56275bc2687d9693411159551684a9c76f943
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522703"
---
# <span data-ttu-id="3ac5f-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="3ac5f-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="3ac5f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ac5f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ac5f-103">Skapa eller uppdatera ett program.</span><span class="sxs-lookup"><span data-stu-id="3ac5f-103">Create or update an application.</span></span>

## <span data-ttu-id="3ac5f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ac5f-104">SYNTAX</span></span>

### <span data-ttu-id="3ac5f-105">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="3ac5f-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-FilePath <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3ac5f-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="3ac5f-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3ac5f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ac5f-107">DESCRIPTION</span></span>
<span data-ttu-id="3ac5f-108">Skapa eller uppdatera ett program.</span><span class="sxs-lookup"><span data-stu-id="3ac5f-108">Create or update an application.</span></span>

## <span data-ttu-id="3ac5f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ac5f-109">EXAMPLES</span></span>

### <span data-ttu-id="3ac5f-110">Exempel 1: skapa ett virtuellt Skriv bords program för Windows</span><span class="sxs-lookup"><span data-stu-id="3ac5f-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> New-AzWvdApplication -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name ApplicationName `
                             -FilePath 'C:\windows\system32\mspaint.exe' `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `
                             -IconIndex 0 `
                             -IconPath 'C:\windows\system32\mspaint.exe' `
                             -CommandLineSetting 'Allow' `
                             -ShowInPortal:$true

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="3ac5f-111">Det här kommandot skapar ett virtuellt Windows-program i en applicaton-grupp.</span><span class="sxs-lookup"><span data-stu-id="3ac5f-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="3ac5f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ac5f-112">PARAMETERS</span></span>

### <span data-ttu-id="3ac5f-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="3ac5f-113">-AppAlias</span></span>
<span data-ttu-id="3ac5f-114">Program Ali Aset från Start-menyn</span><span class="sxs-lookup"><span data-stu-id="3ac5f-114">App Alias from start menu item</span></span>

```yaml
Type: System.String
Parameter Sets: AppAlias
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac5f-115">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="3ac5f-115">-ApplicationType</span></span>
<span data-ttu-id="3ac5f-116">Resurs typ för program.</span><span class="sxs-lookup"><span data-stu-id="3ac5f-116">Resource Type of Application.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RemoteApplicationType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac5f-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="3ac5f-117">-CommandLineArgument</span></span>
<span data-ttu-id="3ac5f-118">Kommando rads argument för programmet.</span><span class="sxs-lookup"><span data-stu-id="3ac5f-118">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="3ac5f-119">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="3ac5f-119">-CommandLineSetting</span></span>
<span data-ttu-id="3ac5f-120">Anger om det här publicerade programmet kan startas med kommando rads argument som tillhandahålls av klienten, kommando rads argument som angetts vid publicerings tillfället eller inga kommando rads argument alls.</span><span class="sxs-lookup"><span data-stu-id="3ac5f-120">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac5f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ac5f-121">-DefaultProfile</span></span>
<span data-ttu-id="3ac5f-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ac5f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ac5f-123">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="3ac5f-123">-Description</span></span>
<span data-ttu-id="3ac5f-124">Beskrivning av program.</span><span class="sxs-lookup"><span data-stu-id="3ac5f-124">Description of Application.</span></span>

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

### <span data-ttu-id="3ac5f-125">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="3ac5f-125">-FilePath</span></span>
<span data-ttu-id="3ac5f-126">Anger en sökväg till den körbara filen för programmet.</span><span class="sxs-lookup"><span data-stu-id="3ac5f-126">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="3ac5f-127">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3ac5f-127">-FriendlyName</span></span>
<span data-ttu-id="3ac5f-128">Eget namn på programmet.</span><span class="sxs-lookup"><span data-stu-id="3ac5f-128">Friendly name of Application.</span></span>

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

### <span data-ttu-id="3ac5f-129">-Grupp namn</span><span class="sxs-lookup"><span data-stu-id="3ac5f-129">-GroupName</span></span>
<span data-ttu-id="3ac5f-130">Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="3ac5f-130">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac5f-131">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="3ac5f-131">-IconIndex</span></span>
<span data-ttu-id="3ac5f-132">Index för ikonen.</span><span class="sxs-lookup"><span data-stu-id="3ac5f-132">Index of the icon.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac5f-133">-IconPath</span><span class="sxs-lookup"><span data-stu-id="3ac5f-133">-IconPath</span></span>
<span data-ttu-id="3ac5f-134">Ikonen Path.</span><span class="sxs-lookup"><span data-stu-id="3ac5f-134">Path to icon.</span></span>

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

### <span data-ttu-id="3ac5f-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="3ac5f-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="3ac5f-136">Anger paket programmets ID för MSIX-program</span><span class="sxs-lookup"><span data-stu-id="3ac5f-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="3ac5f-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="3ac5f-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="3ac5f-138">Anger namnet på paket familjen för MSIX-program</span><span class="sxs-lookup"><span data-stu-id="3ac5f-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="3ac5f-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="3ac5f-139">-Name</span></span>
<span data-ttu-id="3ac5f-140">Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="3ac5f-140">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="3ac5f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ac5f-141">-ResourceGroupName</span></span>
<span data-ttu-id="3ac5f-142">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3ac5f-142">The name of the resource group.</span></span>
<span data-ttu-id="3ac5f-143">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="3ac5f-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3ac5f-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="3ac5f-144">-ShowInPortal</span></span>
<span data-ttu-id="3ac5f-145">Anger om RemoteApp-programmet ska visas i servern för webb åtkomst för fjärr skrivbord.</span><span class="sxs-lookup"><span data-stu-id="3ac5f-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="3ac5f-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ac5f-146">-SubscriptionId</span></span>
<span data-ttu-id="3ac5f-147">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3ac5f-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3ac5f-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3ac5f-148">-Confirm</span></span>
<span data-ttu-id="3ac5f-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3ac5f-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ac5f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ac5f-150">-WhatIf</span></span>
<span data-ttu-id="3ac5f-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3ac5f-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ac5f-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3ac5f-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ac5f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ac5f-153">CommonParameters</span></span>
<span data-ttu-id="3ac5f-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ac5f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ac5f-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ac5f-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ac5f-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ac5f-156">INPUTS</span></span>

## <span data-ttu-id="3ac5f-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ac5f-157">OUTPUTS</span></span>

### <span data-ttu-id="3ac5f-158">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20201102Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="3ac5f-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="3ac5f-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ac5f-159">NOTES</span></span>

<span data-ttu-id="3ac5f-160">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3ac5f-160">ALIASES</span></span>

## <span data-ttu-id="3ac5f-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ac5f-161">RELATED LINKS</span></span>

