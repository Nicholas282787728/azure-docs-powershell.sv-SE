---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 7a78404c8dde734f756792b85d27d712b5c5ed69
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320032"
---
# <span data-ttu-id="3408e-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="3408e-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="3408e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3408e-102">SYNOPSIS</span></span>
<span data-ttu-id="3408e-103">Skapa eller uppdatera ett program.</span><span class="sxs-lookup"><span data-stu-id="3408e-103">Create or update an application.</span></span>

## <span data-ttu-id="3408e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3408e-104">SYNTAX</span></span>

### <span data-ttu-id="3408e-105">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="3408e-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-CommandLineArgument <String>] [-FilePath <String>] [-IconIndex <Int32>]
 [-IconPath <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3408e-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="3408e-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3408e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3408e-107">DESCRIPTION</span></span>
<span data-ttu-id="3408e-108">Skapa eller uppdatera ett program.</span><span class="sxs-lookup"><span data-stu-id="3408e-108">Create or update an application.</span></span>

## <span data-ttu-id="3408e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3408e-109">EXAMPLES</span></span>

### <span data-ttu-id="3408e-110">Exempel 1: skapa ett virtuellt Skriv bords program för Windows</span><span class="sxs-lookup"><span data-stu-id="3408e-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="3408e-111">Det här kommandot skapar ett virtuellt Windows-program i en applicaton-grupp.</span><span class="sxs-lookup"><span data-stu-id="3408e-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="3408e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3408e-112">PARAMETERS</span></span>

### <span data-ttu-id="3408e-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="3408e-113">-AppAlias</span></span>
<span data-ttu-id="3408e-114">Program Ali Aset från Start-menyn</span><span class="sxs-lookup"><span data-stu-id="3408e-114">App Alias from start menu item</span></span>

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

### <span data-ttu-id="3408e-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="3408e-115">-CommandLineArgument</span></span>
<span data-ttu-id="3408e-116">Kommando rads argument för programmet.</span><span class="sxs-lookup"><span data-stu-id="3408e-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="3408e-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="3408e-117">-CommandLineSetting</span></span>
<span data-ttu-id="3408e-118">Anger om det här publicerade programmet kan startas med kommando rads argument som tillhandahålls av klienten, kommando rads argument som angetts vid publicerings tillfället eller inga kommando rads argument alls.</span><span class="sxs-lookup"><span data-stu-id="3408e-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="3408e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3408e-119">-DefaultProfile</span></span>
<span data-ttu-id="3408e-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3408e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3408e-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="3408e-121">-Description</span></span>
<span data-ttu-id="3408e-122">Beskrivning av program.</span><span class="sxs-lookup"><span data-stu-id="3408e-122">Description of Application.</span></span>

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

### <span data-ttu-id="3408e-123">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="3408e-123">-FilePath</span></span>
<span data-ttu-id="3408e-124">Anger en sökväg till den körbara filen för programmet.</span><span class="sxs-lookup"><span data-stu-id="3408e-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="3408e-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3408e-125">-FriendlyName</span></span>
<span data-ttu-id="3408e-126">Eget namn på programmet.</span><span class="sxs-lookup"><span data-stu-id="3408e-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="3408e-127">-Grupp namn</span><span class="sxs-lookup"><span data-stu-id="3408e-127">-GroupName</span></span>
<span data-ttu-id="3408e-128">Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="3408e-128">The name of the application group</span></span>

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

### <span data-ttu-id="3408e-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="3408e-129">-IconIndex</span></span>
<span data-ttu-id="3408e-130">Index för ikonen.</span><span class="sxs-lookup"><span data-stu-id="3408e-130">Index of the icon.</span></span>

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

### <span data-ttu-id="3408e-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="3408e-131">-IconPath</span></span>
<span data-ttu-id="3408e-132">Ikonen Path.</span><span class="sxs-lookup"><span data-stu-id="3408e-132">Path to icon.</span></span>

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

### <span data-ttu-id="3408e-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="3408e-133">-Name</span></span>
<span data-ttu-id="3408e-134">Namnet på programmet i den angivna program gruppen</span><span class="sxs-lookup"><span data-stu-id="3408e-134">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="3408e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3408e-135">-ResourceGroupName</span></span>
<span data-ttu-id="3408e-136">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3408e-136">The name of the resource group.</span></span>
<span data-ttu-id="3408e-137">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="3408e-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3408e-138">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="3408e-138">-ShowInPortal</span></span>
<span data-ttu-id="3408e-139">Anger om RemoteApp-programmet ska visas i servern för webb åtkomst för fjärr skrivbord.</span><span class="sxs-lookup"><span data-stu-id="3408e-139">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="3408e-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3408e-140">-SubscriptionId</span></span>
<span data-ttu-id="3408e-141">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3408e-141">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3408e-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3408e-142">-Confirm</span></span>
<span data-ttu-id="3408e-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3408e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3408e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3408e-144">-WhatIf</span></span>
<span data-ttu-id="3408e-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3408e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3408e-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3408e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3408e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3408e-147">CommonParameters</span></span>
<span data-ttu-id="3408e-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3408e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3408e-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3408e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3408e-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3408e-150">INPUTS</span></span>

## <span data-ttu-id="3408e-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3408e-151">OUTPUTS</span></span>

### <span data-ttu-id="3408e-152">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20191210Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="3408e-152">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="3408e-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3408e-153">NOTES</span></span>

<span data-ttu-id="3408e-154">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3408e-154">ALIASES</span></span>

## <span data-ttu-id="3408e-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3408e-155">RELATED LINKS</span></span>

