---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 38b11543140a0f789674e4109db8cc73c7843f02
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746040"
---
# <span data-ttu-id="d3689-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3689-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="d3689-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3689-102">SYNOPSIS</span></span>

## <span data-ttu-id="d3689-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3689-103">SYNTAX</span></span>

### <span data-ttu-id="d3689-104">S</span><span class="sxs-lookup"><span data-stu-id="d3689-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3689-105">S2</span><span class="sxs-lookup"><span data-stu-id="d3689-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3689-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3689-106">DESCRIPTION</span></span>
<span data-ttu-id="d3689-107">Cmdleten **Remove-AzWebAppSlot** tar bort en Azure Web App-plats med resurs gruppen och namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="d3689-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="d3689-108">Denna cmdlet är som standard också alla kort platser och mått.</span><span class="sxs-lookup"><span data-stu-id="d3689-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="d3689-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3689-109">EXAMPLES</span></span>

### <span data-ttu-id="d3689-110">Exempel 1: ta bort en webb programs plats</span><span class="sxs-lookup"><span data-stu-id="d3689-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="d3689-111">Det här kommandot tar bort platsen med namnet Slot001 associerat med Web App-ContosoSite som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="d3689-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d3689-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3689-112">PARAMETERS</span></span>

### <span data-ttu-id="d3689-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3689-113">-AsJob</span></span>
<span data-ttu-id="d3689-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d3689-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3689-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3689-115">-DefaultProfile</span></span>
<span data-ttu-id="d3689-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d3689-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3689-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d3689-117">-Force</span></span>
<span data-ttu-id="d3689-118">Framtvinga borttagnings alternativ</span><span class="sxs-lookup"><span data-stu-id="d3689-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="d3689-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="d3689-119">-Name</span></span>
<span data-ttu-id="d3689-120">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="d3689-120">WebApp Name</span></span>

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

### <span data-ttu-id="d3689-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3689-121">-ResourceGroupName</span></span>
<span data-ttu-id="d3689-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d3689-122">Resource Group Name</span></span>

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

### <span data-ttu-id="d3689-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="d3689-123">-Slot</span></span>
<span data-ttu-id="d3689-124">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="d3689-124">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3689-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d3689-125">-WebApp</span></span>
<span data-ttu-id="d3689-126">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="d3689-126">WebApp Object</span></span>

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

### <span data-ttu-id="d3689-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d3689-127">-Confirm</span></span>
<span data-ttu-id="d3689-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d3689-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3689-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3689-129">-WhatIf</span></span>
<span data-ttu-id="d3689-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d3689-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3689-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d3689-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3689-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3689-132">CommonParameters</span></span>
<span data-ttu-id="d3689-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3689-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3689-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3689-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3689-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3689-135">INPUTS</span></span>

### <span data-ttu-id="d3689-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d3689-136">System.String</span></span>

### <span data-ttu-id="d3689-137">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="d3689-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d3689-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3689-138">OUTPUTS</span></span>

### <span data-ttu-id="d3689-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d3689-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="d3689-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3689-140">NOTES</span></span>

## <span data-ttu-id="d3689-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3689-141">RELATED LINKS</span></span>

[<span data-ttu-id="d3689-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3689-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="d3689-143">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3689-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="d3689-144">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3689-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="d3689-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3689-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="d3689-146">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3689-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="d3689-147">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d3689-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="d3689-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d3689-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
