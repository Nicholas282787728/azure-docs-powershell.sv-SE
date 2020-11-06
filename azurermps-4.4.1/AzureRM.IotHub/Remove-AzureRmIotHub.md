---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
ms.openlocfilehash: 0f3a6bfa99a199a737c7a69d151d29f5918cc502
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582404"
---
# <span data-ttu-id="2b7e3-101">Remove-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="2b7e3-101">Remove-AzureRmIotHub</span></span>

## <span data-ttu-id="2b7e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2b7e3-102">SYNOPSIS</span></span>
<span data-ttu-id="2b7e3-103">Tar bort en IotHub.</span><span class="sxs-lookup"><span data-stu-id="2b7e3-103">Deletes an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b7e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2b7e3-104">SYNTAX</span></span>

```
Remove-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b7e3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2b7e3-105">DESCRIPTION</span></span>
<span data-ttu-id="2b7e3-106">Tar bort en IotHub.</span><span class="sxs-lookup"><span data-stu-id="2b7e3-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="2b7e3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2b7e3-107">EXAMPLES</span></span>

### <span data-ttu-id="2b7e3-108">Exempel 1 ta bort en IotHub</span><span class="sxs-lookup"><span data-stu-id="2b7e3-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="2b7e3-109">Tar bort en IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="2b7e3-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="2b7e3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2b7e3-110">PARAMETERS</span></span>

### <span data-ttu-id="2b7e3-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="2b7e3-111">-Name</span></span>
<span data-ttu-id="2b7e3-112">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="2b7e3-112">Name of the IotHub</span></span>

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

### <span data-ttu-id="2b7e3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b7e3-113">-ResourceGroupName</span></span>
<span data-ttu-id="2b7e3-114">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="2b7e3-114">Resource Group Name</span></span>

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

### <span data-ttu-id="2b7e3-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2b7e3-115">-Confirm</span></span>
<span data-ttu-id="2b7e3-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2b7e3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b7e3-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b7e3-117">-WhatIf</span></span>
<span data-ttu-id="2b7e3-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2b7e3-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b7e3-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2b7e3-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b7e3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b7e3-120">-DefaultProfile</span></span>
<span data-ttu-id="2b7e3-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2b7e3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b7e3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b7e3-122">CommonParameters</span></span>
<span data-ttu-id="2b7e3-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b7e3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b7e3-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b7e3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b7e3-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2b7e3-125">INPUTS</span></span>

### <span data-ttu-id="2b7e3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2b7e3-126">System.String</span></span>

## <span data-ttu-id="2b7e3-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2b7e3-127">OUTPUTS</span></span>

### <span data-ttu-id="2b7e3-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="2b7e3-128">System.Object</span></span>

## <span data-ttu-id="2b7e3-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2b7e3-129">NOTES</span></span>

## <span data-ttu-id="2b7e3-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2b7e3-130">RELATED LINKS</span></span>

