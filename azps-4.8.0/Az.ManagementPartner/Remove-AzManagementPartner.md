---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: db87797573d3f6c06b52aa072773c9af1a1be1fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102252"
---
# <span data-ttu-id="3e960-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="3e960-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="3e960-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e960-102">SYNOPSIS</span></span>
<span data-ttu-id="3e960-103">Ta bort Microsoft Partner Network (MPN) ID för den aktuella autentiserade användaren eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="3e960-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="3e960-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e960-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e960-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e960-105">DESCRIPTION</span></span>
<span data-ttu-id="3e960-106">Ta bort Microsoft Partner Network (MPN) ID för den aktuella autentiserade användaren eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="3e960-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="3e960-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e960-107">EXAMPLES</span></span>

### <span data-ttu-id="3e960-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3e960-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="3e960-109">Ta bort en hanterings partner</span><span class="sxs-lookup"><span data-stu-id="3e960-109">Remove management partner</span></span>

## <span data-ttu-id="3e960-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e960-110">PARAMETERS</span></span>

### <span data-ttu-id="3e960-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e960-111">-DefaultProfile</span></span>
<span data-ttu-id="3e960-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e960-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e960-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="3e960-113">-PartnerId</span></span>
<span data-ttu-id="3e960-114">ID för hanterings partnern är det ett 6 siffrors nummer</span><span class="sxs-lookup"><span data-stu-id="3e960-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e960-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e960-115">-PassThru</span></span>
<span data-ttu-id="3e960-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3e960-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3e960-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3e960-117">-Confirm</span></span>
<span data-ttu-id="3e960-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3e960-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e960-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e960-119">-WhatIf</span></span>
<span data-ttu-id="3e960-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3e960-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e960-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3e960-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e960-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e960-122">CommonParameters</span></span>
<span data-ttu-id="3e960-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e960-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e960-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e960-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e960-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e960-125">INPUTS</span></span>

### <span data-ttu-id="3e960-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="3e960-126">None</span></span>

## <span data-ttu-id="3e960-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e960-127">OUTPUTS</span></span>

### <span data-ttu-id="3e960-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3e960-128">System.Boolean</span></span>

## <span data-ttu-id="3e960-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e960-129">NOTES</span></span>

## <span data-ttu-id="3e960-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e960-130">RELATED LINKS</span></span>

[<span data-ttu-id="3e960-131">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="3e960-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="3e960-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="3e960-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="3e960-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="3e960-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)