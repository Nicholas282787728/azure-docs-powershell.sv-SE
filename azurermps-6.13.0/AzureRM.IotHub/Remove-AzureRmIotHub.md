---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
ms.openlocfilehash: 674105b31c06d3def687bfc58f8b16be1c6b86f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576971"
---
# <span data-ttu-id="74f60-101">Remove-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="74f60-101">Remove-AzureRmIotHub</span></span>

## <span data-ttu-id="74f60-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74f60-102">SYNOPSIS</span></span>
<span data-ttu-id="74f60-103">Tar bort en IotHub.</span><span class="sxs-lookup"><span data-stu-id="74f60-103">Deletes an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74f60-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74f60-104">SYNTAX</span></span>

```
Remove-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74f60-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74f60-105">DESCRIPTION</span></span>
<span data-ttu-id="74f60-106">Tar bort en IotHub.</span><span class="sxs-lookup"><span data-stu-id="74f60-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="74f60-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74f60-107">EXAMPLES</span></span>

### <span data-ttu-id="74f60-108">Exempel 1 ta bort en IotHub</span><span class="sxs-lookup"><span data-stu-id="74f60-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="74f60-109">Tar bort en IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="74f60-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="74f60-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74f60-110">PARAMETERS</span></span>

### <span data-ttu-id="74f60-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f60-111">-DefaultProfile</span></span>
<span data-ttu-id="74f60-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="74f60-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74f60-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="74f60-113">-Name</span></span>
<span data-ttu-id="74f60-114">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="74f60-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="74f60-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74f60-115">-ResourceGroupName</span></span>
<span data-ttu-id="74f60-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="74f60-116">Resource Group Name</span></span>

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

### <span data-ttu-id="74f60-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="74f60-117">-Confirm</span></span>
<span data-ttu-id="74f60-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="74f60-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74f60-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74f60-119">-WhatIf</span></span>
<span data-ttu-id="74f60-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="74f60-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74f60-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="74f60-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74f60-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f60-122">CommonParameters</span></span>
<span data-ttu-id="74f60-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74f60-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f60-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74f60-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f60-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74f60-125">INPUTS</span></span>

### <span data-ttu-id="74f60-126">System. String</span><span class="sxs-lookup"><span data-stu-id="74f60-126">System.String</span></span>

## <span data-ttu-id="74f60-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74f60-127">OUTPUTS</span></span>

### <span data-ttu-id="74f60-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="74f60-128">System.Void</span></span>

## <span data-ttu-id="74f60-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74f60-129">NOTES</span></span>

## <span data-ttu-id="74f60-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74f60-130">RELATED LINKS</span></span>