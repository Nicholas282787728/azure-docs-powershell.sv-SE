---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 40b14128ec2a1dc48cf098a2c0427728c34c7e22
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923306"
---
# <span data-ttu-id="c7f46-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7f46-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="c7f46-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7f46-102">SYNOPSIS</span></span>
<span data-ttu-id="c7f46-103">Tar bort en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c7f46-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="c7f46-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7f46-104">SYNTAX</span></span>

### <span data-ttu-id="c7f46-105">S</span><span class="sxs-lookup"><span data-stu-id="c7f46-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7f46-106">S2</span><span class="sxs-lookup"><span data-stu-id="c7f46-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-WebApp] <Site> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7f46-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7f46-107">DESCRIPTION</span></span>
<span data-ttu-id="c7f46-108">Cmdleten **Remove-AzWebApp** tar bort en Azure Web App från resurs gruppen och namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="c7f46-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="c7f46-109">Denna cmdlet är som standard också alla kort platser och mått.</span><span class="sxs-lookup"><span data-stu-id="c7f46-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="c7f46-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7f46-110">EXAMPLES</span></span>

### <span data-ttu-id="c7f46-111">Exempel 1: ta bort ett webb program</span><span class="sxs-lookup"><span data-stu-id="c7f46-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="c7f46-112">Det här kommandot tar bort Azure Web App med namnet ContosoSite som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="c7f46-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="c7f46-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7f46-113">PARAMETERS</span></span>

### <span data-ttu-id="c7f46-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7f46-114">-DefaultProfile</span></span>
<span data-ttu-id="c7f46-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c7f46-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7f46-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c7f46-116">-Force</span></span>
<span data-ttu-id="c7f46-117">Framtvinga borttagnings alternativ</span><span class="sxs-lookup"><span data-stu-id="c7f46-117">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="c7f46-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="c7f46-118">-Name</span></span>
<span data-ttu-id="c7f46-119">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="c7f46-119">WebApp Name</span></span>

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

### <span data-ttu-id="c7f46-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7f46-120">-ResourceGroupName</span></span>
<span data-ttu-id="c7f46-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c7f46-121">Resource Group Name</span></span>

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

### <span data-ttu-id="c7f46-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c7f46-122">-WebApp</span></span>
<span data-ttu-id="c7f46-123">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="c7f46-123">WebApp Object</span></span>

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

### <span data-ttu-id="c7f46-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c7f46-124">-Confirm</span></span>
<span data-ttu-id="c7f46-125">Du uppmanas att bekräfta innan du kör cmdleten. Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c7f46-125">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7f46-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7f46-126">-WhatIf</span></span>
<span data-ttu-id="c7f46-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c7f46-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7f46-128">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c7f46-128">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7f46-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c7f46-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7f46-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7f46-130">-AsJob</span></span>
<span data-ttu-id="c7f46-131">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c7f46-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7f46-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7f46-132">CommonParameters</span></span>
<span data-ttu-id="c7f46-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7f46-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7f46-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7f46-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7f46-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7f46-135">INPUTS</span></span>

### <span data-ttu-id="c7f46-136">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="c7f46-136">Site</span></span>
<span data-ttu-id="c7f46-137">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c7f46-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c7f46-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7f46-138">OUTPUTS</span></span>

## <span data-ttu-id="c7f46-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7f46-139">NOTES</span></span>

## <span data-ttu-id="c7f46-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7f46-140">RELATED LINKS</span></span>

[<span data-ttu-id="c7f46-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7f46-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="c7f46-142">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7f46-142">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="c7f46-143">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7f46-143">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="c7f46-144">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7f46-144">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="c7f46-145">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7f46-145">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


