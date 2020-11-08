---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: ddf728a1340d763c1feb2ba313a2dc73494b5d30
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260866"
---
# <span data-ttu-id="47fdd-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="47fdd-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="47fdd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47fdd-102">SYNOPSIS</span></span>
<span data-ttu-id="47fdd-103">Öppnar en fjärrsession för PowerShell i Windows-behållaren som anges på en viss webbplats eller i en viss resurs grupp</span><span class="sxs-lookup"><span data-stu-id="47fdd-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="47fdd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47fdd-104">SYNTAX</span></span>

### <span data-ttu-id="47fdd-105">S1 (standard)</span><span class="sxs-lookup"><span data-stu-id="47fdd-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47fdd-106">S2</span><span class="sxs-lookup"><span data-stu-id="47fdd-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47fdd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47fdd-107">DESCRIPTION</span></span>
<span data-ttu-id="47fdd-108">öppnar en fjärrsession för PowerShell i Windows-behållaren som anges på en viss webbplats eller i en viss resurs grupp</span><span class="sxs-lookup"><span data-stu-id="47fdd-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="47fdd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47fdd-109">EXAMPLES</span></span>

### <span data-ttu-id="47fdd-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="47fdd-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="47fdd-111">Det här kommandot öppnar en fjärrsession för PowerShell till Windows-ContosoASP</span><span class="sxs-lookup"><span data-stu-id="47fdd-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="47fdd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47fdd-112">PARAMETERS</span></span>

### <span data-ttu-id="47fdd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47fdd-113">-DefaultProfile</span></span>
<span data-ttu-id="47fdd-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="47fdd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47fdd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="47fdd-115">-Force</span></span>
<span data-ttu-id="47fdd-116">Skapa PowerShell-sessionen utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="47fdd-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="47fdd-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="47fdd-117">-Name</span></span>
<span data-ttu-id="47fdd-118">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="47fdd-118">The name of the web app.</span></span>

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

### <span data-ttu-id="47fdd-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47fdd-119">-PassThru</span></span>
<span data-ttu-id="47fdd-120">Returnera ett värde som anger om det lyckades eller inte</span><span class="sxs-lookup"><span data-stu-id="47fdd-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="47fdd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47fdd-121">-ResourceGroupName</span></span>
<span data-ttu-id="47fdd-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="47fdd-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="47fdd-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="47fdd-123">-SlotName</span></span>
<span data-ttu-id="47fdd-124">Namnet på Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="47fdd-124">The name of the web app slot.</span></span>

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

### <span data-ttu-id="47fdd-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="47fdd-125">-WebApp</span></span>
<span data-ttu-id="47fdd-126">Web App-objekt</span><span class="sxs-lookup"><span data-stu-id="47fdd-126">The web app object</span></span>

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

### <span data-ttu-id="47fdd-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="47fdd-127">-Confirm</span></span>
<span data-ttu-id="47fdd-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="47fdd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47fdd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47fdd-129">-WhatIf</span></span>
<span data-ttu-id="47fdd-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="47fdd-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47fdd-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="47fdd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47fdd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47fdd-132">CommonParameters</span></span>
<span data-ttu-id="47fdd-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47fdd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47fdd-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47fdd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47fdd-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47fdd-135">INPUTS</span></span>

### <span data-ttu-id="47fdd-136">System. String</span><span class="sxs-lookup"><span data-stu-id="47fdd-136">System.String</span></span>

### <span data-ttu-id="47fdd-137">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="47fdd-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="47fdd-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47fdd-138">OUTPUTS</span></span>

### <span data-ttu-id="47fdd-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="47fdd-139">System.Void</span></span>

## <span data-ttu-id="47fdd-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47fdd-140">NOTES</span></span>

## <span data-ttu-id="47fdd-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47fdd-141">RELATED LINKS</span></span>
