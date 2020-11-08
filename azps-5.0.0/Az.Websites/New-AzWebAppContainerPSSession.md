---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
ms.openlocfilehash: 2244eb06257d69005d64cc640d0ecd783bd30572
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271665"
---
# <span data-ttu-id="b890a-101">New-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="b890a-101">New-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="b890a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b890a-102">SYNOPSIS</span></span>
<span data-ttu-id="b890a-103">New-AzWebAppContainerPSSession skapar en ny fjärrsession för PowerShell till Windows-behållaren som anges på en viss webbplats eller i en viss resurs grupp</span><span class="sxs-lookup"><span data-stu-id="b890a-103">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="b890a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b890a-104">SYNTAX</span></span>

### <span data-ttu-id="b890a-105">S1 (standard)</span><span class="sxs-lookup"><span data-stu-id="b890a-105">S1 (Default)</span></span>
```
New-AzWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b890a-106">S2</span><span class="sxs-lookup"><span data-stu-id="b890a-106">S2</span></span>
```
New-AzWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b890a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b890a-107">DESCRIPTION</span></span>
<span data-ttu-id="b890a-108">New-AzWebAppContainerPSSession skapar en ny fjärrsession för PowerShell till Windows-behållaren som anges på en viss webbplats eller i en viss resurs grupp</span><span class="sxs-lookup"><span data-stu-id="b890a-108">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="b890a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b890a-109">EXAMPLES</span></span>

### <span data-ttu-id="b890a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b890a-110">Example 1</span></span>
```
PS C:\> $s = New-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="b890a-111">Detta skapar en ny fjärrsession för PowerShell till Windows-testprogrammet ContosoASP och visar processerna som körs på behållaren ContosoASP</span><span class="sxs-lookup"><span data-stu-id="b890a-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="b890a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b890a-112">PARAMETERS</span></span>

### <span data-ttu-id="b890a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b890a-113">-DefaultProfile</span></span>
<span data-ttu-id="b890a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b890a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b890a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b890a-115">-Force</span></span>
<span data-ttu-id="b890a-116">Skapa PowerShell-sessionen utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="b890a-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b890a-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="b890a-117">-Name</span></span>
<span data-ttu-id="b890a-118">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="b890a-118">The name of the web app.</span></span>

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

### <span data-ttu-id="b890a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b890a-119">-ResourceGroupName</span></span>
<span data-ttu-id="b890a-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b890a-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="b890a-121">-SlotName</span><span class="sxs-lookup"><span data-stu-id="b890a-121">-SlotName</span></span>
<span data-ttu-id="b890a-122">Namnet på Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="b890a-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="b890a-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b890a-123">-WebApp</span></span>
<span data-ttu-id="b890a-124">Web App-objekt</span><span class="sxs-lookup"><span data-stu-id="b890a-124">The web app object</span></span>

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

### <span data-ttu-id="b890a-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b890a-125">-Confirm</span></span>
<span data-ttu-id="b890a-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b890a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b890a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b890a-127">-WhatIf</span></span>
<span data-ttu-id="b890a-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b890a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b890a-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b890a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b890a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b890a-130">CommonParameters</span></span>
<span data-ttu-id="b890a-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b890a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b890a-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b890a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b890a-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b890a-133">INPUTS</span></span>

### <span data-ttu-id="b890a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b890a-134">System.String</span></span>

### <span data-ttu-id="b890a-135">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="b890a-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b890a-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b890a-136">OUTPUTS</span></span>

### <span data-ttu-id="b890a-137">System. Management. Automation. Runspaces. PSSession</span><span class="sxs-lookup"><span data-stu-id="b890a-137">System.Management.Automation.Runspaces.PSSession</span></span>

## <span data-ttu-id="b890a-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b890a-138">NOTES</span></span>

## <span data-ttu-id="b890a-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b890a-139">RELATED LINKS</span></span>
