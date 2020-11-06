---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/update-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
ms.openlocfilehash: 76abdc2f7a7099529af87f69af8e37319685aea7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576429"
---
# <span data-ttu-id="48147-101">Update-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="48147-101">Update-AzureRmReservation</span></span>

## <span data-ttu-id="48147-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48147-102">SYNOPSIS</span></span>
<span data-ttu-id="48147-103">Uppdatera a `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="48147-103">Update a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48147-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48147-104">SYNTAX</span></span>

### <span data-ttu-id="48147-105">CommandLine (standard)</span><span class="sxs-lookup"><span data-stu-id="48147-105">CommandLine (Default)</span></span>
```
Update-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -AppliedScopeType <String>
 [-AppliedScope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48147-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="48147-106">PipeObject</span></span>
```
Update-AzureRmReservation -AppliedScopeType <String> [-AppliedScope <String>] -Reservation <PSReservation>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48147-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48147-107">DESCRIPTION</span></span>
<span data-ttu-id="48147-108">Uppdaterar tillämpliga omfattningar för `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="48147-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="48147-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48147-109">EXAMPLES</span></span>

### <span data-ttu-id="48147-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="48147-110">Example 1</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="48147-111">Uppdaterar AppliedScopeType för angiven reservation till Single</span><span class="sxs-lookup"><span data-stu-id="48147-111">Updates the AppliedScopeType of the specified reservation to Single</span></span>

### <span data-ttu-id="48147-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="48147-112">Example 2</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared"
```

<span data-ttu-id="48147-113">Uppdaterar AppliedScopeType för angiven reservation till delad</span><span class="sxs-lookup"><span data-stu-id="48147-113">Updates the AppliedScopeType of the specified reservation to Shared</span></span>

## <span data-ttu-id="48147-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48147-114">PARAMETERS</span></span>

### <span data-ttu-id="48147-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="48147-115">-AppliedScope</span></span>
<span data-ttu-id="48147-116">SubscriptionId för `Reservation` att det ska användas</span><span class="sxs-lookup"><span data-stu-id="48147-116">SubscriptionId for this `Reservation` to be applied</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48147-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="48147-117">-AppliedScopeType</span></span>
<span data-ttu-id="48147-118">Typ av `Reservation` uppdatering</span><span class="sxs-lookup"><span data-stu-id="48147-118">Type of the `Reservation` to be updated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Single, Shared

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48147-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48147-119">-DefaultProfile</span></span>
<span data-ttu-id="48147-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="48147-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48147-121">-Reservation</span><span class="sxs-lookup"><span data-stu-id="48147-121">-Reservation</span></span>
<span data-ttu-id="48147-122">Pipe-objekttyp för `Reservation`</span><span class="sxs-lookup"><span data-stu-id="48147-122">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48147-123">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="48147-123">-ReservationId</span></span>
<span data-ttu-id="48147-124">ID för `Reservation` till-uppdateringen</span><span class="sxs-lookup"><span data-stu-id="48147-124">Id of the `Reservation` to update</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48147-125">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="48147-125">-ReservationOrderId</span></span>
<span data-ttu-id="48147-126">ID för `ReservationOrder` till-uppdateringen</span><span class="sxs-lookup"><span data-stu-id="48147-126">Id of the `ReservationOrder` to update</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48147-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="48147-127">-Confirm</span></span>
<span data-ttu-id="48147-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="48147-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48147-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48147-129">-WhatIf</span></span>
<span data-ttu-id="48147-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="48147-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48147-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="48147-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48147-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48147-132">CommonParameters</span></span>
<span data-ttu-id="48147-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48147-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48147-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48147-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48147-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48147-135">INPUTS</span></span>

### <span data-ttu-id="48147-136">Microsoft. Azure. commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="48147-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="48147-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48147-137">OUTPUTS</span></span>

### <span data-ttu-id="48147-138">Microsoft. Azure. commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="48147-138">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="48147-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48147-139">NOTES</span></span>

## <span data-ttu-id="48147-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48147-140">RELATED LINKS</span></span>

