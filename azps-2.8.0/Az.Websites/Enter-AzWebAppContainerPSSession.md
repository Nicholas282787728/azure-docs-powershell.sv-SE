---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: b18008268ffd07369cf527c53d6ad693a38d85f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921116"
---
# <span data-ttu-id="ea675-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="ea675-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="ea675-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea675-102">SYNOPSIS</span></span>
<span data-ttu-id="ea675-103">Öppnar en fjärrsession för PowerShell i Windows-behållaren som anges på en viss webbplats eller i en viss resurs grupp</span><span class="sxs-lookup"><span data-stu-id="ea675-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="ea675-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea675-104">SYNTAX</span></span>

### <span data-ttu-id="ea675-105">S1 (standard)</span><span class="sxs-lookup"><span data-stu-id="ea675-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea675-106">S2</span><span class="sxs-lookup"><span data-stu-id="ea675-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea675-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea675-107">DESCRIPTION</span></span>
<span data-ttu-id="ea675-108">öppnar en fjärrsession för PowerShell i Windows-behållaren som anges på en viss webbplats eller i en viss resurs grupp</span><span class="sxs-lookup"><span data-stu-id="ea675-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="ea675-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea675-109">EXAMPLES</span></span>

### <span data-ttu-id="ea675-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ea675-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="ea675-111">Det här kommandot öppnar en fjärrsession för PowerShell till Windows-ContosoASP</span><span class="sxs-lookup"><span data-stu-id="ea675-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="ea675-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea675-112">PARAMETERS</span></span>

### <span data-ttu-id="ea675-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea675-113">-DefaultProfile</span></span>
<span data-ttu-id="ea675-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ea675-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea675-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ea675-115">-Force</span></span>
<span data-ttu-id="ea675-116">Skapa PowerShell-sessionen utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="ea675-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ea675-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="ea675-117">-Name</span></span>
<span data-ttu-id="ea675-118">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="ea675-118">The name of the web app.</span></span>

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

### <span data-ttu-id="ea675-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea675-119">-PassThru</span></span>
<span data-ttu-id="ea675-120">Returnera ett värde som anger om det lyckades eller inte</span><span class="sxs-lookup"><span data-stu-id="ea675-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="ea675-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea675-121">-ResourceGroupName</span></span>
<span data-ttu-id="ea675-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ea675-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="ea675-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="ea675-123">-SlotName</span></span>
<span data-ttu-id="ea675-124">Namnet på Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="ea675-124">The name of the web app slot.</span></span>

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

### <span data-ttu-id="ea675-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ea675-125">-WebApp</span></span>
<span data-ttu-id="ea675-126">Web App-objekt</span><span class="sxs-lookup"><span data-stu-id="ea675-126">The web app object</span></span>

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

### <span data-ttu-id="ea675-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ea675-127">-Confirm</span></span>
<span data-ttu-id="ea675-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ea675-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea675-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea675-129">-WhatIf</span></span>
<span data-ttu-id="ea675-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ea675-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea675-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ea675-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea675-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea675-132">CommonParameters</span></span>
<span data-ttu-id="ea675-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea675-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea675-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea675-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea675-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea675-135">INPUTS</span></span>

### <span data-ttu-id="ea675-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ea675-136">System.String</span></span>

### <span data-ttu-id="ea675-137">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="ea675-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ea675-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea675-138">OUTPUTS</span></span>

### <span data-ttu-id="ea675-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="ea675-139">System.Void</span></span>

## <span data-ttu-id="ea675-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea675-140">NOTES</span></span>

## <span data-ttu-id="ea675-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea675-141">RELATED LINKS</span></span>
