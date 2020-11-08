---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
ms.openlocfilehash: 2244eb06257d69005d64cc640d0ecd783bd30572
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260850"
---
# <span data-ttu-id="ece58-101">New-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="ece58-101">New-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="ece58-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ece58-102">SYNOPSIS</span></span>
<span data-ttu-id="ece58-103">New-AzWebAppContainerPSSession skapar en ny fjärrsession för PowerShell till Windows-behållaren som anges på en viss webbplats eller i en viss resurs grupp</span><span class="sxs-lookup"><span data-stu-id="ece58-103">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="ece58-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ece58-104">SYNTAX</span></span>

### <span data-ttu-id="ece58-105">S1 (standard)</span><span class="sxs-lookup"><span data-stu-id="ece58-105">S1 (Default)</span></span>
```
New-AzWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ece58-106">S2</span><span class="sxs-lookup"><span data-stu-id="ece58-106">S2</span></span>
```
New-AzWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ece58-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ece58-107">DESCRIPTION</span></span>
<span data-ttu-id="ece58-108">New-AzWebAppContainerPSSession skapar en ny fjärrsession för PowerShell till Windows-behållaren som anges på en viss webbplats eller i en viss resurs grupp</span><span class="sxs-lookup"><span data-stu-id="ece58-108">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="ece58-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ece58-109">EXAMPLES</span></span>

### <span data-ttu-id="ece58-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ece58-110">Example 1</span></span>
```
PS C:\> $s = New-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="ece58-111">Detta skapar en ny fjärrsession för PowerShell till Windows-testprogrammet ContosoASP och visar processerna som körs på behållaren ContosoASP</span><span class="sxs-lookup"><span data-stu-id="ece58-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="ece58-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ece58-112">PARAMETERS</span></span>

### <span data-ttu-id="ece58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece58-113">-DefaultProfile</span></span>
<span data-ttu-id="ece58-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ece58-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ece58-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ece58-115">-Force</span></span>
<span data-ttu-id="ece58-116">Skapa PowerShell-sessionen utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="ece58-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ece58-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="ece58-117">-Name</span></span>
<span data-ttu-id="ece58-118">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="ece58-118">The name of the web app.</span></span>

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

### <span data-ttu-id="ece58-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ece58-119">-ResourceGroupName</span></span>
<span data-ttu-id="ece58-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ece58-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="ece58-121">-SlotName</span><span class="sxs-lookup"><span data-stu-id="ece58-121">-SlotName</span></span>
<span data-ttu-id="ece58-122">Namnet på Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="ece58-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="ece58-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ece58-123">-WebApp</span></span>
<span data-ttu-id="ece58-124">Web App-objekt</span><span class="sxs-lookup"><span data-stu-id="ece58-124">The web app object</span></span>

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

### <span data-ttu-id="ece58-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ece58-125">-Confirm</span></span>
<span data-ttu-id="ece58-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ece58-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ece58-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ece58-127">-WhatIf</span></span>
<span data-ttu-id="ece58-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ece58-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ece58-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ece58-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ece58-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece58-130">CommonParameters</span></span>
<span data-ttu-id="ece58-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ece58-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece58-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ece58-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece58-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ece58-133">INPUTS</span></span>

### <span data-ttu-id="ece58-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ece58-134">System.String</span></span>

### <span data-ttu-id="ece58-135">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="ece58-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ece58-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ece58-136">OUTPUTS</span></span>

### <span data-ttu-id="ece58-137">System. Management. Automation. Runspaces. PSSession</span><span class="sxs-lookup"><span data-stu-id="ece58-137">System.Management.Automation.Runspaces.PSSession</span></span>

## <span data-ttu-id="ece58-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ece58-138">NOTES</span></span>

## <span data-ttu-id="ece58-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ece58-139">RELATED LINKS</span></span>
