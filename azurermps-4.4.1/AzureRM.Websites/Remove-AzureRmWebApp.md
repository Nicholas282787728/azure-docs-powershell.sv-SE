---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
ms.openlocfilehash: b903e22a627ca2cb992b179e8f6956d556558b6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585244"
---
# <span data-ttu-id="a744c-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a744c-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="a744c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a744c-102">SYNOPSIS</span></span>
<span data-ttu-id="a744c-103">Tar bort en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a744c-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a744c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a744c-104">SYNTAX</span></span>

### <span data-ttu-id="a744c-105">S</span><span class="sxs-lookup"><span data-stu-id="a744c-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a744c-106">S2</span><span class="sxs-lookup"><span data-stu-id="a744c-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a744c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a744c-107">DESCRIPTION</span></span>
<span data-ttu-id="a744c-108">Cmdleten **Remove-AzureRmWebApp** tar bort en Azure Web App från resurs gruppen och namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="a744c-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="a744c-109">Denna cmdlet är som standard också alla kort platser och mått.</span><span class="sxs-lookup"><span data-stu-id="a744c-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="a744c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a744c-110">EXAMPLES</span></span>

### <span data-ttu-id="a744c-111">Exempel 1: ta bort ett webb program</span><span class="sxs-lookup"><span data-stu-id="a744c-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="a744c-112">Det här kommandot tar bort Azure Web App med namnet ContosoSite som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="a744c-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a744c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a744c-113">PARAMETERS</span></span>

### <span data-ttu-id="a744c-114">-Force</span><span class="sxs-lookup"><span data-stu-id="a744c-114">-Force</span></span>
<span data-ttu-id="a744c-115">Framtvinga borttagnings alternativ</span><span class="sxs-lookup"><span data-stu-id="a744c-115">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="a744c-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="a744c-116">-Name</span></span>
<span data-ttu-id="a744c-117">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="a744c-117">WebApp Name</span></span>

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

### <span data-ttu-id="a744c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a744c-118">-ResourceGroupName</span></span>
<span data-ttu-id="a744c-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a744c-119">Resource Group Name</span></span>

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

### <span data-ttu-id="a744c-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a744c-120">-WebApp</span></span>
<span data-ttu-id="a744c-121">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="a744c-121">WebApp Object</span></span>

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

### <span data-ttu-id="a744c-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a744c-122">-Confirm</span></span>
<span data-ttu-id="a744c-123">Du uppmanas att bekräfta innan du kör cmdleten. Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a744c-123">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a744c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a744c-124">-WhatIf</span></span>
<span data-ttu-id="a744c-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a744c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a744c-126">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a744c-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a744c-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a744c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a744c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a744c-128">-DefaultProfile</span></span>
<span data-ttu-id="a744c-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a744c-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a744c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a744c-130">CommonParameters</span></span>
<span data-ttu-id="a744c-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a744c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a744c-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a744c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a744c-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a744c-133">INPUTS</span></span>

### <span data-ttu-id="a744c-134">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="a744c-134">Site</span></span>
<span data-ttu-id="a744c-135">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a744c-135">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a744c-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a744c-136">OUTPUTS</span></span>

## <span data-ttu-id="a744c-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a744c-137">NOTES</span></span>

## <span data-ttu-id="a744c-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a744c-138">RELATED LINKS</span></span>

[<span data-ttu-id="a744c-139">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a744c-139">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="a744c-140">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a744c-140">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="a744c-141">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a744c-141">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="a744c-142">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a744c-142">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="a744c-143">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a744c-143">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


