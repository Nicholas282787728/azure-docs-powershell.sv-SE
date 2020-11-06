---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppContainerPSSession.md
ms.openlocfilehash: 3c5efcd51a8b546acb5fa9b8ed3623c40ddfb1e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573821"
---
# <span data-ttu-id="24d44-101">New-AzureRmWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="24d44-101">New-AzureRmWebAppContainerPSSession</span></span>

## <span data-ttu-id="24d44-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24d44-102">SYNOPSIS</span></span>
<span data-ttu-id="24d44-103">New-AzureRmWebAppContainerPSSession skapar en ny fjärrsession för PowerShell till Windows-behållaren som anges på en viss webbplats eller i en viss resurs grupp</span><span class="sxs-lookup"><span data-stu-id="24d44-103">New-AzureRmWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24d44-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24d44-104">SYNTAX</span></span>

### <span data-ttu-id="24d44-105">S1 (standard)</span><span class="sxs-lookup"><span data-stu-id="24d44-105">S1 (Default)</span></span>
```
New-AzureRmWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24d44-106">S2</span><span class="sxs-lookup"><span data-stu-id="24d44-106">S2</span></span>
```
New-AzureRmWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24d44-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24d44-107">DESCRIPTION</span></span>
<span data-ttu-id="24d44-108">New-AzureRmWebAppContainerPSSession skapar en ny fjärrsession för PowerShell till Windows-behållaren som anges på en viss webbplats eller i en viss resurs grupp</span><span class="sxs-lookup"><span data-stu-id="24d44-108">New-AzureRmWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="24d44-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24d44-109">EXAMPLES</span></span>

### <span data-ttu-id="24d44-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="24d44-110">Example 1</span></span>
```
PS C:\> $s = New-AzureRmWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="24d44-111">Detta skapar en ny fjärrsession för PowerShell till Windows-testprogrammet ContosoASP och visar processerna som körs på behållaren ContosoASP</span><span class="sxs-lookup"><span data-stu-id="24d44-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="24d44-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24d44-112">PARAMETERS</span></span>

### <span data-ttu-id="24d44-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d44-113">-DefaultProfile</span></span>
<span data-ttu-id="24d44-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="24d44-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24d44-115">-Force</span><span class="sxs-lookup"><span data-stu-id="24d44-115">-Force</span></span>
<span data-ttu-id="24d44-116">Skapa PowerShell-sessionen utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="24d44-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="24d44-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="24d44-117">-Name</span></span>
<span data-ttu-id="24d44-118">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="24d44-118">The name of the web app.</span></span>

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

### <span data-ttu-id="24d44-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24d44-119">-ResourceGroupName</span></span>
<span data-ttu-id="24d44-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="24d44-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="24d44-121">-SlotName</span><span class="sxs-lookup"><span data-stu-id="24d44-121">-SlotName</span></span>
<span data-ttu-id="24d44-122">Namnet på Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="24d44-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="24d44-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="24d44-123">-WebApp</span></span>
<span data-ttu-id="24d44-124">Web App-objekt</span><span class="sxs-lookup"><span data-stu-id="24d44-124">The web app object</span></span>

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

### <span data-ttu-id="24d44-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="24d44-125">-Confirm</span></span>
<span data-ttu-id="24d44-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="24d44-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24d44-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24d44-127">-WhatIf</span></span>
<span data-ttu-id="24d44-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="24d44-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24d44-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="24d44-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24d44-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d44-130">CommonParameters</span></span>
<span data-ttu-id="24d44-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24d44-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d44-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24d44-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d44-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24d44-133">INPUTS</span></span>

### <span data-ttu-id="24d44-134">System. String</span><span class="sxs-lookup"><span data-stu-id="24d44-134">System.String</span></span>
### <span data-ttu-id="24d44-135">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="24d44-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="24d44-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24d44-136">OUTPUTS</span></span>

### <span data-ttu-id="24d44-137">System. String</span><span class="sxs-lookup"><span data-stu-id="24d44-137">System.String</span></span>
## <span data-ttu-id="24d44-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24d44-138">NOTES</span></span>

## <span data-ttu-id="24d44-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24d44-139">RELATED LINKS</span></span>
