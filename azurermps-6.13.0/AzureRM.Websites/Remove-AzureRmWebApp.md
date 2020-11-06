---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
ms.openlocfilehash: b06a5253ac5b26097d2dc4dea9c3d557c00a4d46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573819"
---
# <span data-ttu-id="46e81-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46e81-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="46e81-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46e81-102">SYNOPSIS</span></span>
<span data-ttu-id="46e81-103">Tar bort en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="46e81-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46e81-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46e81-104">SYNTAX</span></span>

### <span data-ttu-id="46e81-105">S</span><span class="sxs-lookup"><span data-stu-id="46e81-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46e81-106">S2</span><span class="sxs-lookup"><span data-stu-id="46e81-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46e81-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46e81-107">DESCRIPTION</span></span>
<span data-ttu-id="46e81-108">Cmdleten **Remove-AzureRmWebApp** tar bort en Azure Web App från resurs gruppen och namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="46e81-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="46e81-109">Denna cmdlet är som standard också alla kort platser och mått.</span><span class="sxs-lookup"><span data-stu-id="46e81-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="46e81-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46e81-110">EXAMPLES</span></span>

### <span data-ttu-id="46e81-111">Exempel 1: ta bort ett webb program</span><span class="sxs-lookup"><span data-stu-id="46e81-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="46e81-112">Det här kommandot tar bort Azure Web App med namnet ContosoSite som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="46e81-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="46e81-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46e81-113">PARAMETERS</span></span>

### <span data-ttu-id="46e81-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46e81-114">-AsJob</span></span>
<span data-ttu-id="46e81-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="46e81-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46e81-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46e81-116">-DefaultProfile</span></span>
<span data-ttu-id="46e81-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="46e81-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46e81-118">-Force</span><span class="sxs-lookup"><span data-stu-id="46e81-118">-Force</span></span>
<span data-ttu-id="46e81-119">Framtvinga borttagnings alternativ</span><span class="sxs-lookup"><span data-stu-id="46e81-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="46e81-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="46e81-120">-Name</span></span>
<span data-ttu-id="46e81-121">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="46e81-121">WebApp Name</span></span>

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

### <span data-ttu-id="46e81-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46e81-122">-ResourceGroupName</span></span>
<span data-ttu-id="46e81-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="46e81-123">Resource Group Name</span></span>

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

### <span data-ttu-id="46e81-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="46e81-124">-WebApp</span></span>
<span data-ttu-id="46e81-125">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="46e81-125">WebApp Object</span></span>

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

### <span data-ttu-id="46e81-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="46e81-126">-Confirm</span></span>
<span data-ttu-id="46e81-127">Du uppmanas att bekräfta innan du kör cmdleten. Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="46e81-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46e81-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46e81-128">-WhatIf</span></span>
<span data-ttu-id="46e81-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="46e81-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46e81-130">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="46e81-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46e81-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="46e81-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46e81-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e81-132">CommonParameters</span></span>
<span data-ttu-id="46e81-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46e81-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e81-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46e81-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e81-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46e81-135">INPUTS</span></span>

### <span data-ttu-id="46e81-136">System. String</span><span class="sxs-lookup"><span data-stu-id="46e81-136">System.String</span></span>

### <span data-ttu-id="46e81-137">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="46e81-137">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="46e81-138">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="46e81-138">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="46e81-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46e81-139">OUTPUTS</span></span>

### <span data-ttu-id="46e81-140">System. Void</span><span class="sxs-lookup"><span data-stu-id="46e81-140">System.Void</span></span>

## <span data-ttu-id="46e81-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46e81-141">NOTES</span></span>

## <span data-ttu-id="46e81-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46e81-142">RELATED LINKS</span></span>

[<span data-ttu-id="46e81-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46e81-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="46e81-144">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46e81-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="46e81-145">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46e81-145">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="46e81-146">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46e81-146">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="46e81-147">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="46e81-147">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


