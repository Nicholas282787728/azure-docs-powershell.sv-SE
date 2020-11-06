---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: 65393bc3dd2e9e6b51699a21baf0e6d3750464bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585239"
---
# <span data-ttu-id="b0758-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0758-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="b0758-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0758-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0758-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0758-103">SYNTAX</span></span>

### <span data-ttu-id="b0758-104">S</span><span class="sxs-lookup"><span data-stu-id="b0758-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0758-105">S2</span><span class="sxs-lookup"><span data-stu-id="b0758-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0758-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0758-106">DESCRIPTION</span></span>
<span data-ttu-id="b0758-107">Cmdleten **Remove-AzureRmWebAppSlot** tar bort en Azure Web App-plats med resurs gruppen och namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="b0758-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="b0758-108">Denna cmdlet är som standard också alla kort platser och mått.</span><span class="sxs-lookup"><span data-stu-id="b0758-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="b0758-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0758-109">EXAMPLES</span></span>

### <span data-ttu-id="b0758-110">Exempel 1: ta bort en webb programs plats</span><span class="sxs-lookup"><span data-stu-id="b0758-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="b0758-111">Det här kommandot tar bort platsen med namnet Slot001 associerat med Web App-ContosoSite som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="b0758-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="b0758-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0758-112">PARAMETERS</span></span>

### <span data-ttu-id="b0758-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b0758-113">-Force</span></span>
<span data-ttu-id="b0758-114">Framtvinga borttagnings alternativ</span><span class="sxs-lookup"><span data-stu-id="b0758-114">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="b0758-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="b0758-115">-Name</span></span>
<span data-ttu-id="b0758-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="b0758-116">WebApp Name</span></span>

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

### <span data-ttu-id="b0758-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0758-117">-ResourceGroupName</span></span>
<span data-ttu-id="b0758-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="b0758-118">Resource Group Name</span></span>

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

### <span data-ttu-id="b0758-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="b0758-119">-Slot</span></span>
<span data-ttu-id="b0758-120">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="b0758-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="b0758-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b0758-121">-WebApp</span></span>
<span data-ttu-id="b0758-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="b0758-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0758-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b0758-123">-Confirm</span></span>
<span data-ttu-id="b0758-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b0758-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0758-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0758-125">-WhatIf</span></span>
<span data-ttu-id="b0758-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b0758-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0758-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b0758-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0758-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0758-128">-DefaultProfile</span></span>
<span data-ttu-id="b0758-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b0758-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0758-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0758-130">CommonParameters</span></span>
<span data-ttu-id="b0758-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0758-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0758-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0758-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0758-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0758-133">INPUTS</span></span>

### <span data-ttu-id="b0758-134">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="b0758-134">Site</span></span>
<span data-ttu-id="b0758-135">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b0758-135">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b0758-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0758-136">OUTPUTS</span></span>

### <span data-ttu-id="b0758-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b0758-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="b0758-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0758-138">NOTES</span></span>

## <span data-ttu-id="b0758-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0758-139">RELATED LINKS</span></span>

[<span data-ttu-id="b0758-140">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0758-140">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="b0758-141">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0758-141">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="b0758-142">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0758-142">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="b0758-143">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0758-143">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="b0758-144">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0758-144">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="b0758-145">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0758-145">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="b0758-146">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b0758-146">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
