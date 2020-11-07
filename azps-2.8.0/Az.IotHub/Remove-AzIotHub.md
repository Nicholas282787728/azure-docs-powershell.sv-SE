---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 1529b7b70ec25a7ee8f4b047e28fe77efaf92351
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743976"
---
# <span data-ttu-id="1af30-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="1af30-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="1af30-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1af30-102">SYNOPSIS</span></span>
<span data-ttu-id="1af30-103">Tar bort en IotHub.</span><span class="sxs-lookup"><span data-stu-id="1af30-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="1af30-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1af30-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1af30-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1af30-105">DESCRIPTION</span></span>
<span data-ttu-id="1af30-106">Tar bort en IotHub.</span><span class="sxs-lookup"><span data-stu-id="1af30-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="1af30-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1af30-107">EXAMPLES</span></span>

### <span data-ttu-id="1af30-108">Exempel 1 ta bort en IotHub</span><span class="sxs-lookup"><span data-stu-id="1af30-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="1af30-109">Tar bort en IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="1af30-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="1af30-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1af30-110">PARAMETERS</span></span>

### <span data-ttu-id="1af30-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af30-111">-DefaultProfile</span></span>
<span data-ttu-id="1af30-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1af30-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1af30-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="1af30-113">-Name</span></span>
<span data-ttu-id="1af30-114">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="1af30-114">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af30-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af30-115">-ResourceGroupName</span></span>
<span data-ttu-id="1af30-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="1af30-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af30-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1af30-117">-Confirm</span></span>
<span data-ttu-id="1af30-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1af30-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1af30-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1af30-119">-WhatIf</span></span>
<span data-ttu-id="1af30-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1af30-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1af30-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1af30-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1af30-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af30-122">CommonParameters</span></span>
<span data-ttu-id="1af30-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1af30-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af30-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1af30-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af30-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1af30-125">INPUTS</span></span>

### <span data-ttu-id="1af30-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1af30-126">System.String</span></span>

## <span data-ttu-id="1af30-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1af30-127">OUTPUTS</span></span>

### <span data-ttu-id="1af30-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="1af30-128">System.Void</span></span>

## <span data-ttu-id="1af30-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1af30-129">NOTES</span></span>

## <span data-ttu-id="1af30-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1af30-130">RELATED LINKS</span></span>
