---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: 7fdf5e8de2ec326888c57e8219a006f9ef447aa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577756"
---
# <span data-ttu-id="94944-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="94944-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="94944-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94944-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94944-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94944-103">SYNTAX</span></span>

### <span data-ttu-id="94944-104">S</span><span class="sxs-lookup"><span data-stu-id="94944-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94944-105">S2</span><span class="sxs-lookup"><span data-stu-id="94944-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94944-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94944-106">DESCRIPTION</span></span>
<span data-ttu-id="94944-107">Cmdleten **Remove-AzureRmWebAppSlot** tar bort en Azure Web App-plats med resurs gruppen och namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="94944-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="94944-108">Denna cmdlet är som standard också alla kort platser och mått.</span><span class="sxs-lookup"><span data-stu-id="94944-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="94944-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94944-109">EXAMPLES</span></span>

### <span data-ttu-id="94944-110">Exempel 1: ta bort en webb programs plats</span><span class="sxs-lookup"><span data-stu-id="94944-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="94944-111">Det här kommandot tar bort platsen med namnet Slot001 associerat med Web App-ContosoSite som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="94944-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="94944-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94944-112">PARAMETERS</span></span>

### <span data-ttu-id="94944-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94944-113">-AsJob</span></span>
<span data-ttu-id="94944-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="94944-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94944-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94944-115">-DefaultProfile</span></span>
<span data-ttu-id="94944-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="94944-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94944-117">-Force</span><span class="sxs-lookup"><span data-stu-id="94944-117">-Force</span></span>
<span data-ttu-id="94944-118">Framtvinga borttagnings alternativ</span><span class="sxs-lookup"><span data-stu-id="94944-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="94944-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="94944-119">-Name</span></span>
<span data-ttu-id="94944-120">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="94944-120">WebApp Name</span></span>

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

### <span data-ttu-id="94944-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94944-121">-ResourceGroupName</span></span>
<span data-ttu-id="94944-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="94944-122">Resource Group Name</span></span>

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

### <span data-ttu-id="94944-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="94944-123">-Slot</span></span>
<span data-ttu-id="94944-124">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="94944-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="94944-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="94944-125">-WebApp</span></span>
<span data-ttu-id="94944-126">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="94944-126">WebApp Object</span></span>

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

### <span data-ttu-id="94944-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="94944-127">-Confirm</span></span>
<span data-ttu-id="94944-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="94944-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94944-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94944-129">-WhatIf</span></span>
<span data-ttu-id="94944-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="94944-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94944-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="94944-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94944-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94944-132">CommonParameters</span></span>
<span data-ttu-id="94944-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94944-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94944-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94944-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94944-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94944-135">INPUTS</span></span>

### <span data-ttu-id="94944-136">System. String</span><span class="sxs-lookup"><span data-stu-id="94944-136">System.String</span></span>

### <span data-ttu-id="94944-137">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="94944-137">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="94944-138">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="94944-138">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="94944-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94944-139">OUTPUTS</span></span>

### <span data-ttu-id="94944-140">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="94944-140">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="94944-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94944-141">NOTES</span></span>

## <span data-ttu-id="94944-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94944-142">RELATED LINKS</span></span>

[<span data-ttu-id="94944-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="94944-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="94944-144">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="94944-144">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="94944-145">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="94944-145">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="94944-146">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="94944-146">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="94944-147">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="94944-147">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="94944-148">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="94944-148">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="94944-149">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="94944-149">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
