---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: 0631492bf2574fed7a9bb755088d811483504763
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921176"
---
# <span data-ttu-id="d5054-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="d5054-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="d5054-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d5054-102">SYNOPSIS</span></span>
<span data-ttu-id="d5054-103">Tar bort en regel för åtkomst begränsning från en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d5054-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="d5054-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d5054-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> -Name <String>
 [-TargetScmSite] [-SlotName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5054-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d5054-105">DESCRIPTION</span></span>
<span data-ttu-id="d5054-106">Cmdleten **Remove-AzWebAppAccessRestrictionRule** tar bort en begränsnings regel för åtkomst från en Azure Web App</span><span class="sxs-lookup"><span data-stu-id="d5054-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="d5054-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d5054-107">EXAMPLES</span></span>

### <span data-ttu-id="d5054-108">Exempel 1: ta bort en begränsnings regel för webb program</span><span class="sxs-lookup"><span data-stu-id="d5054-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="d5054-109">Det här kommandot tar bort regeln för begränsning av IpRule från Azure Web App med namnet ContosoSite som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="d5054-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d5054-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d5054-110">PARAMETERS</span></span>

### <span data-ttu-id="d5054-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5054-111">-DefaultProfile</span></span>
<span data-ttu-id="d5054-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d5054-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5054-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="d5054-113">-Name</span></span>
<span data-ttu-id="d5054-114">Namn på regel för åtkomst begränsning</span><span class="sxs-lookup"><span data-stu-id="d5054-114">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="d5054-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5054-115">-PassThru</span></span>
<span data-ttu-id="d5054-116">Returnera konfigurations objekt för åtkomst begränsning.</span><span class="sxs-lookup"><span data-stu-id="d5054-116">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="d5054-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5054-117">-ResourceGroupName</span></span>
<span data-ttu-id="d5054-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d5054-118">Resource Group Name</span></span>

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

### <span data-ttu-id="d5054-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="d5054-119">-SlotName</span></span>
<span data-ttu-id="d5054-120">Namn på distributions platsen.</span><span class="sxs-lookup"><span data-stu-id="d5054-120">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="d5054-121">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="d5054-121">-TargetScmSite</span></span>
<span data-ttu-id="d5054-122">Regeln är avsedd för huvud webbplatsen eller SCM-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="d5054-122">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="d5054-123">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="d5054-123">-WebAppName</span></span>
<span data-ttu-id="d5054-124">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="d5054-124">The name of the web app.</span></span>

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

### <span data-ttu-id="d5054-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d5054-125">-Confirm</span></span>
<span data-ttu-id="d5054-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d5054-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5054-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5054-127">-WhatIf</span></span>
<span data-ttu-id="d5054-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d5054-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5054-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d5054-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5054-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5054-130">CommonParameters</span></span>
<span data-ttu-id="d5054-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5054-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5054-132">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5054-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5054-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d5054-133">INPUTS</span></span>

### <span data-ttu-id="d5054-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d5054-134">System.String</span></span>

## <span data-ttu-id="d5054-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d5054-135">OUTPUTS</span></span>

### <span data-ttu-id="d5054-136">Microsoft. Azure. commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="d5054-136">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="d5054-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d5054-137">NOTES</span></span>

## <span data-ttu-id="d5054-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d5054-138">RELATED LINKS</span></span>

[<span data-ttu-id="d5054-139">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="d5054-139">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="d5054-140">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="d5054-140">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="d5054-141">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="d5054-141">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
