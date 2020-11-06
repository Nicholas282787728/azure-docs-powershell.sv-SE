---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393045
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Remove-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Remove-AzureRmManagementPartner.md
ms.openlocfilehash: 3bb1b54abf947d5fc2a05538cc31ce53fb794ab7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584171"
---
# <span data-ttu-id="64b6e-101">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="64b6e-101">Remove-AzureRmManagementPartner</span></span>

## <span data-ttu-id="64b6e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="64b6e-102">SYNOPSIS</span></span>
<span data-ttu-id="64b6e-103">Ta bort Microsoft Partner Network (MPN) ID för den aktuella autentiserade användaren eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="64b6e-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64b6e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="64b6e-104">SYNTAX</span></span>

```
Remove-AzureRmManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64b6e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="64b6e-105">DESCRIPTION</span></span>
<span data-ttu-id="64b6e-106">Ta bort Microsoft Partner Network (MPN) ID för den aktuella autentiserade användaren eller tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="64b6e-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="64b6e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="64b6e-107">EXAMPLES</span></span>

### <span data-ttu-id="64b6e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="64b6e-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzureRmManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="64b6e-109">Ta bort en hanterings partner</span><span class="sxs-lookup"><span data-stu-id="64b6e-109">Remove management partner</span></span> 

## <span data-ttu-id="64b6e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="64b6e-110">PARAMETERS</span></span>

### <span data-ttu-id="64b6e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64b6e-111">-DefaultProfile</span></span>
<span data-ttu-id="64b6e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="64b6e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64b6e-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="64b6e-113">-PartnerId</span></span>
<span data-ttu-id="64b6e-114">ID för hanterings partnern är det ett 6 siffrors nummer</span><span class="sxs-lookup"><span data-stu-id="64b6e-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="64b6e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64b6e-115">-PassThru</span></span>
<span data-ttu-id="64b6e-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="64b6e-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="64b6e-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="64b6e-117">-Confirm</span></span>
<span data-ttu-id="64b6e-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="64b6e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64b6e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64b6e-119">-WhatIf</span></span>
<span data-ttu-id="64b6e-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="64b6e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64b6e-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="64b6e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64b6e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64b6e-122">CommonParameters</span></span>
<span data-ttu-id="64b6e-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64b6e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64b6e-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64b6e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64b6e-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="64b6e-125">INPUTS</span></span>

### <span data-ttu-id="64b6e-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="64b6e-126">None</span></span>

## <span data-ttu-id="64b6e-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="64b6e-127">OUTPUTS</span></span>

### <span data-ttu-id="64b6e-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="64b6e-128">System.Boolean</span></span>

## <span data-ttu-id="64b6e-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="64b6e-129">NOTES</span></span>

## <span data-ttu-id="64b6e-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="64b6e-130">RELATED LINKS</span></span>

[<span data-ttu-id="64b6e-131">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="64b6e-131">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="64b6e-132">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="64b6e-132">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)

[<span data-ttu-id="64b6e-133">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="64b6e-133">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
