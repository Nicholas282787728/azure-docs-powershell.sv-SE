---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
ms.openlocfilehash: 1da7b9981b3c2fe96d895290b7ab73dfc36e183e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577194"
---
# <span data-ttu-id="02cd4-101">Remove-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="02cd4-101">Remove-AzureRmIotHub</span></span>

## <span data-ttu-id="02cd4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02cd4-102">SYNOPSIS</span></span>
<span data-ttu-id="02cd4-103">Tar bort en IotHub.</span><span class="sxs-lookup"><span data-stu-id="02cd4-103">Deletes an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02cd4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02cd4-104">SYNTAX</span></span>

```
Remove-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02cd4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02cd4-105">DESCRIPTION</span></span>
<span data-ttu-id="02cd4-106">Tar bort en IotHub.</span><span class="sxs-lookup"><span data-stu-id="02cd4-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="02cd4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02cd4-107">EXAMPLES</span></span>

### <span data-ttu-id="02cd4-108">Exempel 1 ta bort en IotHub</span><span class="sxs-lookup"><span data-stu-id="02cd4-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="02cd4-109">Tar bort en IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="02cd4-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="02cd4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02cd4-110">PARAMETERS</span></span>

### <span data-ttu-id="02cd4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02cd4-111">-DefaultProfile</span></span>
<span data-ttu-id="02cd4-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="02cd4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02cd4-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="02cd4-113">-Name</span></span>
<span data-ttu-id="02cd4-114">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="02cd4-114">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02cd4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02cd4-115">-ResourceGroupName</span></span>
<span data-ttu-id="02cd4-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="02cd4-116">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02cd4-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="02cd4-117">-Confirm</span></span>
<span data-ttu-id="02cd4-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02cd4-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02cd4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02cd4-119">-WhatIf</span></span>
<span data-ttu-id="02cd4-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="02cd4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02cd4-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="02cd4-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02cd4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02cd4-122">CommonParameters</span></span>
<span data-ttu-id="02cd4-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02cd4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02cd4-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02cd4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02cd4-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02cd4-125">INPUTS</span></span>

### <span data-ttu-id="02cd4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="02cd4-126">System.String</span></span>

## <span data-ttu-id="02cd4-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02cd4-127">OUTPUTS</span></span>

### <span data-ttu-id="02cd4-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="02cd4-128">System.Object</span></span>

## <span data-ttu-id="02cd4-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02cd4-129">NOTES</span></span>

## <span data-ttu-id="02cd4-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02cd4-130">RELATED LINKS</span></span>

