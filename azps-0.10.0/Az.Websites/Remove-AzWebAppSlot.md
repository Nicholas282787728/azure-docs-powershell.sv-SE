---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 04813b04d3d2499de549655edb6398550ce25536
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923294"
---
# <span data-ttu-id="ebfc7-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ebfc7-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="ebfc7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ebfc7-102">SYNOPSIS</span></span>

## <span data-ttu-id="ebfc7-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ebfc7-103">SYNTAX</span></span>

### <span data-ttu-id="ebfc7-104">S</span><span class="sxs-lookup"><span data-stu-id="ebfc7-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebfc7-105">S2</span><span class="sxs-lookup"><span data-stu-id="ebfc7-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-WebApp] <Site> [-AsJob][-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebfc7-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ebfc7-106">DESCRIPTION</span></span>
<span data-ttu-id="ebfc7-107">Cmdleten **Remove-AzWebAppSlot** tar bort en Azure Web App-plats med resurs gruppen och namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="ebfc7-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="ebfc7-108">Denna cmdlet är som standard också alla kort platser och mått.</span><span class="sxs-lookup"><span data-stu-id="ebfc7-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="ebfc7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ebfc7-109">EXAMPLES</span></span>

### <span data-ttu-id="ebfc7-110">Exempel 1: ta bort en webb programs plats</span><span class="sxs-lookup"><span data-stu-id="ebfc7-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "ContosoSlot"
```

<span data-ttu-id="ebfc7-111">Det här kommandot tar bort platsen med namnet Slot001 associerat med Web App-ContosoSite som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="ebfc7-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ebfc7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ebfc7-112">PARAMETERS</span></span>

### <span data-ttu-id="ebfc7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebfc7-113">-DefaultProfile</span></span>
<span data-ttu-id="ebfc7-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ebfc7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfc7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ebfc7-115">-Force</span></span>
<span data-ttu-id="ebfc7-116">Framtvinga borttagnings alternativ</span><span class="sxs-lookup"><span data-stu-id="ebfc7-116">Forcefully Remove Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfc7-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="ebfc7-117">-Name</span></span>
<span data-ttu-id="ebfc7-118">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="ebfc7-118">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebfc7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebfc7-119">-ResourceGroupName</span></span>
<span data-ttu-id="ebfc7-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="ebfc7-120">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfc7-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="ebfc7-121">-Slot</span></span>
<span data-ttu-id="ebfc7-122">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="ebfc7-122">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfc7-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ebfc7-123">-WebApp</span></span>
<span data-ttu-id="ebfc7-124">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="ebfc7-124">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebfc7-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ebfc7-125">-Confirm</span></span>
<span data-ttu-id="ebfc7-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ebfc7-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfc7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebfc7-127">-WhatIf</span></span>
<span data-ttu-id="ebfc7-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ebfc7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebfc7-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ebfc7-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="ebfc7-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ebfc7-130">-AsJob</span></span>
<span data-ttu-id="ebfc7-131">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ebfc7-131">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfc7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebfc7-132">CommonParameters</span></span>
<span data-ttu-id="ebfc7-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebfc7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebfc7-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebfc7-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebfc7-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ebfc7-135">INPUTS</span></span>

### <span data-ttu-id="ebfc7-136">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="ebfc7-136">Site</span></span>
<span data-ttu-id="ebfc7-137">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ebfc7-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ebfc7-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ebfc7-138">OUTPUTS</span></span>

### <span data-ttu-id="ebfc7-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ebfc7-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="ebfc7-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ebfc7-140">NOTES</span></span>

## <span data-ttu-id="ebfc7-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ebfc7-141">RELATED LINKS</span></span>

[<span data-ttu-id="ebfc7-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ebfc7-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="ebfc7-143">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ebfc7-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="ebfc7-144">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ebfc7-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="ebfc7-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ebfc7-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="ebfc7-146">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ebfc7-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="ebfc7-147">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ebfc7-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="ebfc7-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ebfc7-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
