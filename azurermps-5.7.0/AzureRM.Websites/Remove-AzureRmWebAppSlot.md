---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: eeaeb43083a2b125147df5d91516b71bdff377a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582892"
---
# <span data-ttu-id="71f82-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71f82-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="71f82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71f82-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71f82-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71f82-103">SYNTAX</span></span>

### <span data-ttu-id="71f82-104">S</span><span class="sxs-lookup"><span data-stu-id="71f82-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71f82-105">S2</span><span class="sxs-lookup"><span data-stu-id="71f82-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-WebApp] <Site> [-AsJob][-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71f82-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71f82-106">DESCRIPTION</span></span>
<span data-ttu-id="71f82-107">Cmdleten **Remove-AzureRmWebAppSlot** tar bort en Azure Web App-plats med resurs gruppen och namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="71f82-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="71f82-108">Denna cmdlet är som standard också alla kort platser och mått.</span><span class="sxs-lookup"><span data-stu-id="71f82-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="71f82-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71f82-109">EXAMPLES</span></span>

### <span data-ttu-id="71f82-110">Exempel 1: ta bort en webb programs plats</span><span class="sxs-lookup"><span data-stu-id="71f82-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "ContosoSlot"
```

<span data-ttu-id="71f82-111">Det här kommandot tar bort platsen med namnet Slot001 associerat med Web App-ContosoSite som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="71f82-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="71f82-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71f82-112">PARAMETERS</span></span>

### <span data-ttu-id="71f82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71f82-113">-DefaultProfile</span></span>
<span data-ttu-id="71f82-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="71f82-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71f82-115">-Force</span><span class="sxs-lookup"><span data-stu-id="71f82-115">-Force</span></span>
<span data-ttu-id="71f82-116">Framtvinga borttagnings alternativ</span><span class="sxs-lookup"><span data-stu-id="71f82-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="71f82-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="71f82-117">-Name</span></span>
<span data-ttu-id="71f82-118">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="71f82-118">WebApp Name</span></span>

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

### <span data-ttu-id="71f82-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71f82-119">-ResourceGroupName</span></span>
<span data-ttu-id="71f82-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="71f82-120">Resource Group Name</span></span>

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

### <span data-ttu-id="71f82-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="71f82-121">-Slot</span></span>
<span data-ttu-id="71f82-122">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="71f82-122">WebApp Slot Name</span></span>

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

### <span data-ttu-id="71f82-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="71f82-123">-WebApp</span></span>
<span data-ttu-id="71f82-124">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="71f82-124">WebApp Object</span></span>

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

### <span data-ttu-id="71f82-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="71f82-125">-Confirm</span></span>
<span data-ttu-id="71f82-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="71f82-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71f82-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71f82-127">-WhatIf</span></span>
<span data-ttu-id="71f82-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="71f82-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71f82-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="71f82-129">The cmdlet is not run.</span></span>

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
### <span data-ttu-id="71f82-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71f82-130">-AsJob</span></span>
<span data-ttu-id="71f82-131">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="71f82-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71f82-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71f82-132">CommonParameters</span></span>
<span data-ttu-id="71f82-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71f82-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71f82-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71f82-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71f82-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71f82-135">INPUTS</span></span>

### <span data-ttu-id="71f82-136">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="71f82-136">Site</span></span>
<span data-ttu-id="71f82-137">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="71f82-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="71f82-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71f82-138">OUTPUTS</span></span>

### <span data-ttu-id="71f82-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="71f82-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="71f82-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71f82-140">NOTES</span></span>

## <span data-ttu-id="71f82-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71f82-141">RELATED LINKS</span></span>

[<span data-ttu-id="71f82-142">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71f82-142">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="71f82-143">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71f82-143">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="71f82-144">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71f82-144">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="71f82-145">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71f82-145">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="71f82-146">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71f82-146">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="71f82-147">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71f82-147">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="71f82-148">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="71f82-148">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
