---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: c91e5ff71a916e28e199a1c64fde2d69f0193fd1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746047"
---
# <span data-ttu-id="1bad3-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1bad3-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="1bad3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1bad3-102">SYNOPSIS</span></span>
<span data-ttu-id="1bad3-103">Tar bort en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1bad3-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="1bad3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1bad3-104">SYNTAX</span></span>

### <span data-ttu-id="1bad3-105">S</span><span class="sxs-lookup"><span data-stu-id="1bad3-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bad3-106">S2</span><span class="sxs-lookup"><span data-stu-id="1bad3-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bad3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1bad3-107">DESCRIPTION</span></span>
<span data-ttu-id="1bad3-108">Cmdleten **Remove-AzWebApp** tar bort en Azure Web App från resurs gruppen och namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="1bad3-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="1bad3-109">Denna cmdlet är som standard också alla kort platser och mått.</span><span class="sxs-lookup"><span data-stu-id="1bad3-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="1bad3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1bad3-110">EXAMPLES</span></span>

### <span data-ttu-id="1bad3-111">Exempel 1: ta bort ett webb program</span><span class="sxs-lookup"><span data-stu-id="1bad3-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="1bad3-112">Det här kommandot tar bort Azure Web App med namnet ContosoSite som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="1bad3-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="1bad3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1bad3-113">PARAMETERS</span></span>

### <span data-ttu-id="1bad3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bad3-114">-AsJob</span></span>
<span data-ttu-id="1bad3-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1bad3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1bad3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bad3-116">-DefaultProfile</span></span>
<span data-ttu-id="1bad3-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1bad3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bad3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1bad3-118">-Force</span></span>
<span data-ttu-id="1bad3-119">Framtvinga borttagnings alternativ</span><span class="sxs-lookup"><span data-stu-id="1bad3-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="1bad3-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="1bad3-120">-Name</span></span>
<span data-ttu-id="1bad3-121">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="1bad3-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bad3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bad3-122">-ResourceGroupName</span></span>
<span data-ttu-id="1bad3-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="1bad3-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bad3-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1bad3-124">-WebApp</span></span>
<span data-ttu-id="1bad3-125">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="1bad3-125">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1bad3-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1bad3-126">-Confirm</span></span>
<span data-ttu-id="1bad3-127">Du uppmanas att bekräfta innan du kör cmdleten. Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1bad3-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bad3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bad3-128">-WhatIf</span></span>
<span data-ttu-id="1bad3-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1bad3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bad3-130">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1bad3-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bad3-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1bad3-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bad3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bad3-132">CommonParameters</span></span>
<span data-ttu-id="1bad3-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bad3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bad3-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bad3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bad3-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1bad3-135">INPUTS</span></span>

### <span data-ttu-id="1bad3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1bad3-136">System.String</span></span>

### <span data-ttu-id="1bad3-137">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="1bad3-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1bad3-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1bad3-138">OUTPUTS</span></span>

### <span data-ttu-id="1bad3-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="1bad3-139">System.Void</span></span>

## <span data-ttu-id="1bad3-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1bad3-140">NOTES</span></span>

## <span data-ttu-id="1bad3-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1bad3-141">RELATED LINKS</span></span>

[<span data-ttu-id="1bad3-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1bad3-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="1bad3-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1bad3-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="1bad3-144">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1bad3-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="1bad3-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1bad3-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="1bad3-146">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1bad3-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

