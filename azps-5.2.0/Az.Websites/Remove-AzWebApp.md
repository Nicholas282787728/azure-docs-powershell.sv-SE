---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 64d463e6cbe3012b8d49e0a61b4f081f286e25b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389379"
---
# <span data-ttu-id="586e5-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="586e5-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="586e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="586e5-102">SYNOPSIS</span></span>
<span data-ttu-id="586e5-103">Tar bort en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="586e5-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="586e5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="586e5-104">SYNTAX</span></span>

### <span data-ttu-id="586e5-105">S</span><span class="sxs-lookup"><span data-stu-id="586e5-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="586e5-106">S2</span><span class="sxs-lookup"><span data-stu-id="586e5-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="586e5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="586e5-107">DESCRIPTION</span></span>
<span data-ttu-id="586e5-108">Cmdleten **Remove-AzWebApp** tar bort en Azure Web App från resurs gruppen och namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="586e5-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="586e5-109">Denna cmdlet är som standard också alla kort platser och mått.</span><span class="sxs-lookup"><span data-stu-id="586e5-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="586e5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="586e5-110">EXAMPLES</span></span>

### <span data-ttu-id="586e5-111">Exempel 1: ta bort ett webb program</span><span class="sxs-lookup"><span data-stu-id="586e5-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="586e5-112">Det här kommandot tar bort Azure Web App med namnet ContosoSite som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="586e5-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="586e5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="586e5-113">PARAMETERS</span></span>

### <span data-ttu-id="586e5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="586e5-114">-AsJob</span></span>
<span data-ttu-id="586e5-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="586e5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="586e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="586e5-116">-DefaultProfile</span></span>
<span data-ttu-id="586e5-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="586e5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="586e5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="586e5-118">-Force</span></span>
<span data-ttu-id="586e5-119">Framtvinga borttagnings alternativ</span><span class="sxs-lookup"><span data-stu-id="586e5-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="586e5-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="586e5-120">-Name</span></span>
<span data-ttu-id="586e5-121">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="586e5-121">WebApp Name</span></span>

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

### <span data-ttu-id="586e5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="586e5-122">-ResourceGroupName</span></span>
<span data-ttu-id="586e5-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="586e5-123">Resource Group Name</span></span>

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

### <span data-ttu-id="586e5-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="586e5-124">-WebApp</span></span>
<span data-ttu-id="586e5-125">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="586e5-125">WebApp Object</span></span>

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

### <span data-ttu-id="586e5-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="586e5-126">-Confirm</span></span>
<span data-ttu-id="586e5-127">Du uppmanas att bekräfta innan du kör cmdleten. Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="586e5-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="586e5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="586e5-128">-WhatIf</span></span>
<span data-ttu-id="586e5-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="586e5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="586e5-130">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="586e5-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="586e5-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="586e5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="586e5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="586e5-132">CommonParameters</span></span>
<span data-ttu-id="586e5-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="586e5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="586e5-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="586e5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="586e5-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="586e5-135">INPUTS</span></span>

### <span data-ttu-id="586e5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="586e5-136">System.String</span></span>

### <span data-ttu-id="586e5-137">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="586e5-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="586e5-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="586e5-138">OUTPUTS</span></span>

### <span data-ttu-id="586e5-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="586e5-139">System.Void</span></span>

## <span data-ttu-id="586e5-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="586e5-140">NOTES</span></span>

## <span data-ttu-id="586e5-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="586e5-141">RELATED LINKS</span></span>

[<span data-ttu-id="586e5-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="586e5-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="586e5-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="586e5-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="586e5-144">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="586e5-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="586e5-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="586e5-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="586e5-146">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="586e5-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


