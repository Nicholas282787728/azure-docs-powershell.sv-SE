---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Enter-AzureRmWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Enter-AzureRmWebAppContainerPSSession.md
ms.openlocfilehash: 350ad76952a2953a107e0626b9cf2e0e8b640bb3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573825"
---
# <span data-ttu-id="af15b-101">Enter-AzureRmWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="af15b-101">Enter-AzureRmWebAppContainerPSSession</span></span>

## <span data-ttu-id="af15b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af15b-102">SYNOPSIS</span></span>
<span data-ttu-id="af15b-103">Öppnar en fjärrsession för PowerShell i Windows-behållaren som anges på en viss webbplats eller i en viss resurs grupp</span><span class="sxs-lookup"><span data-stu-id="af15b-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af15b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af15b-104">SYNTAX</span></span>

### <span data-ttu-id="af15b-105">S1 (standard)</span><span class="sxs-lookup"><span data-stu-id="af15b-105">S1 (Default)</span></span>
```
Enter-AzureRmWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af15b-106">S2</span><span class="sxs-lookup"><span data-stu-id="af15b-106">S2</span></span>
```
Enter-AzureRmWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af15b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af15b-107">DESCRIPTION</span></span>
<span data-ttu-id="af15b-108">öppnar en fjärrsession för PowerShell i Windows-behållaren som anges på en viss webbplats eller i en viss resurs grupp</span><span class="sxs-lookup"><span data-stu-id="af15b-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="af15b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af15b-109">EXAMPLES</span></span>

### <span data-ttu-id="af15b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="af15b-110">Example 1</span></span>
```
PS C:\> Enter-AzureRmWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="af15b-111">Det här kommandot öppnar en fjärrsession för PowerShell till Windows-ContosoASP</span><span class="sxs-lookup"><span data-stu-id="af15b-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="af15b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af15b-112">PARAMETERS</span></span>

### <span data-ttu-id="af15b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af15b-113">-DefaultProfile</span></span>
<span data-ttu-id="af15b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af15b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af15b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="af15b-115">-Force</span></span>
<span data-ttu-id="af15b-116">Skapa PowerShell-sessionen utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="af15b-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="af15b-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="af15b-117">-Name</span></span>
<span data-ttu-id="af15b-118">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="af15b-118">The name of the web app.</span></span>

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

### <span data-ttu-id="af15b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af15b-119">-PassThru</span></span>
<span data-ttu-id="af15b-120">Returnera ett värde som anger om det lyckades eller inte</span><span class="sxs-lookup"><span data-stu-id="af15b-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="af15b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af15b-121">-ResourceGroupName</span></span>
<span data-ttu-id="af15b-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="af15b-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="af15b-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="af15b-123">-SlotName</span></span>
<span data-ttu-id="af15b-124">Namnet på Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="af15b-124">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af15b-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="af15b-125">-WebApp</span></span>
<span data-ttu-id="af15b-126">Web App-objekt</span><span class="sxs-lookup"><span data-stu-id="af15b-126">The web app object</span></span>

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

### <span data-ttu-id="af15b-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="af15b-127">-Confirm</span></span>
<span data-ttu-id="af15b-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="af15b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af15b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af15b-129">-WhatIf</span></span>
<span data-ttu-id="af15b-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="af15b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af15b-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="af15b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af15b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af15b-132">CommonParameters</span></span>
<span data-ttu-id="af15b-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af15b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af15b-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af15b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af15b-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af15b-135">INPUTS</span></span>

### <span data-ttu-id="af15b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="af15b-136">System.String</span></span>
### <span data-ttu-id="af15b-137">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="af15b-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="af15b-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af15b-138">OUTPUTS</span></span>

### <span data-ttu-id="af15b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="af15b-139">System.String</span></span>
## <span data-ttu-id="af15b-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af15b-140">NOTES</span></span>

## <span data-ttu-id="af15b-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af15b-141">RELATED LINKS</span></span>
