---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
ms.openlocfilehash: a984a9a76a41db93bee96acfa029ca05a30d85f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575418"
---
# <span data-ttu-id="ff066-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ff066-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="ff066-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff066-102">SYNOPSIS</span></span>
<span data-ttu-id="ff066-103">Tar bort en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ff066-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff066-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff066-104">SYNTAX</span></span>

### <span data-ttu-id="ff066-105">S</span><span class="sxs-lookup"><span data-stu-id="ff066-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff066-106">S2</span><span class="sxs-lookup"><span data-stu-id="ff066-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-WebApp] <Site> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff066-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff066-107">DESCRIPTION</span></span>
<span data-ttu-id="ff066-108">Cmdleten **Remove-AzureRmWebApp** tar bort en Azure Web App från resurs gruppen och namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="ff066-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="ff066-109">Denna cmdlet är som standard också alla kort platser och mått.</span><span class="sxs-lookup"><span data-stu-id="ff066-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="ff066-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff066-110">EXAMPLES</span></span>

### <span data-ttu-id="ff066-111">Exempel 1: ta bort ett webb program</span><span class="sxs-lookup"><span data-stu-id="ff066-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="ff066-112">Det här kommandot tar bort Azure Web App med namnet ContosoSite som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="ff066-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ff066-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff066-113">PARAMETERS</span></span>

### <span data-ttu-id="ff066-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff066-114">-DefaultProfile</span></span>
<span data-ttu-id="ff066-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff066-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff066-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ff066-116">-Force</span></span>
<span data-ttu-id="ff066-117">Framtvinga borttagnings alternativ</span><span class="sxs-lookup"><span data-stu-id="ff066-117">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="ff066-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ff066-118">-Name</span></span>
<span data-ttu-id="ff066-119">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="ff066-119">WebApp Name</span></span>

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

### <span data-ttu-id="ff066-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff066-120">-ResourceGroupName</span></span>
<span data-ttu-id="ff066-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="ff066-121">Resource Group Name</span></span>

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

### <span data-ttu-id="ff066-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ff066-122">-WebApp</span></span>
<span data-ttu-id="ff066-123">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="ff066-123">WebApp Object</span></span>

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

### <span data-ttu-id="ff066-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ff066-124">-Confirm</span></span>
<span data-ttu-id="ff066-125">Du uppmanas att bekräfta innan du kör cmdleten. Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ff066-125">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff066-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff066-126">-WhatIf</span></span>
<span data-ttu-id="ff066-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ff066-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff066-128">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ff066-128">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff066-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ff066-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff066-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff066-130">-AsJob</span></span>
<span data-ttu-id="ff066-131">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ff066-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ff066-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff066-132">CommonParameters</span></span>
<span data-ttu-id="ff066-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff066-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff066-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff066-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff066-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff066-135">INPUTS</span></span>

### <span data-ttu-id="ff066-136">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="ff066-136">Site</span></span>
<span data-ttu-id="ff066-137">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ff066-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ff066-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff066-138">OUTPUTS</span></span>

## <span data-ttu-id="ff066-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff066-139">NOTES</span></span>

## <span data-ttu-id="ff066-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff066-140">RELATED LINKS</span></span>

[<span data-ttu-id="ff066-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ff066-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="ff066-142">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ff066-142">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="ff066-143">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ff066-143">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="ff066-144">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ff066-144">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="ff066-145">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ff066-145">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


