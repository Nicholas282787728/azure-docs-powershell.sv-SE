---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: 4d4228ebcdf007485e35b45b93ea738c828c9c4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414168"
---
# <span data-ttu-id="666ad-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="666ad-101">Update-AzReservation</span></span>

## <span data-ttu-id="666ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="666ad-102">SYNOPSIS</span></span>
<span data-ttu-id="666ad-103">Uppdatera a `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="666ad-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="666ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="666ad-104">SYNTAX</span></span>

### <span data-ttu-id="666ad-105">CommandLine (standard)</span><span class="sxs-lookup"><span data-stu-id="666ad-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="666ad-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="666ad-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="666ad-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="666ad-107">DESCRIPTION</span></span>
<span data-ttu-id="666ad-108">Uppdaterar tillämpliga omfattningar för `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="666ad-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="666ad-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="666ad-109">EXAMPLES</span></span>

### <span data-ttu-id="666ad-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="666ad-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="666ad-111">Uppdaterar AppliedScopeType för angiven `Reservation` till Single och InstanceFlexibility to on.</span><span class="sxs-lookup"><span data-stu-id="666ad-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="666ad-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="666ad-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="666ad-113">Uppdaterar AppliedScopeType för angiven `Reservation` till delad och InstanceFlexibility till av.</span><span class="sxs-lookup"><span data-stu-id="666ad-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="666ad-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="666ad-114">PARAMETERS</span></span>

### <span data-ttu-id="666ad-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="666ad-115">-AppliedScope</span></span>
<span data-ttu-id="666ad-116">SubscriptionId för `Reservation` att det ska användas</span><span class="sxs-lookup"><span data-stu-id="666ad-116">SubscriptionId for this `Reservation` to be applied</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666ad-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="666ad-117">-AppliedScopeType</span></span>
<span data-ttu-id="666ad-118">Typ av använt scope</span><span class="sxs-lookup"><span data-stu-id="666ad-118">Type of the Applied Scope</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666ad-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="666ad-119">-DefaultProfile</span></span>
<span data-ttu-id="666ad-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="666ad-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="666ad-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="666ad-121">-InstanceFlexibility</span></span>
<span data-ttu-id="666ad-122">Om det visas uppdaterar InstanceFlexibility-värdet för `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="666ad-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="666ad-123">Om inget anges ändras inte det befintliga värdet.</span><span class="sxs-lookup"><span data-stu-id="666ad-123">If not specified, the existing value remains unchanged.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666ad-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="666ad-124">-Name</span></span>
<span data-ttu-id="666ad-125">Reservationens namn</span><span class="sxs-lookup"><span data-stu-id="666ad-125">Name of Reservation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666ad-126">-Reservation</span><span class="sxs-lookup"><span data-stu-id="666ad-126">-Reservation</span></span>
<span data-ttu-id="666ad-127">Pipe-objekttyp för `Reservation`</span><span class="sxs-lookup"><span data-stu-id="666ad-127">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="666ad-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="666ad-128">-ReservationId</span></span>
<span data-ttu-id="666ad-129">ID för `Reservation` till-uppdateringen</span><span class="sxs-lookup"><span data-stu-id="666ad-129">Id of the `Reservation` to update</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666ad-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="666ad-130">-ReservationOrderId</span></span>
<span data-ttu-id="666ad-131">ID för `ReservationOrder` till-uppdateringen</span><span class="sxs-lookup"><span data-stu-id="666ad-131">Id of the `ReservationOrder` to update</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666ad-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="666ad-132">-Confirm</span></span>
<span data-ttu-id="666ad-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="666ad-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="666ad-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="666ad-134">-WhatIf</span></span>
<span data-ttu-id="666ad-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="666ad-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="666ad-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="666ad-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="666ad-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="666ad-137">CommonParameters</span></span>
<span data-ttu-id="666ad-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="666ad-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="666ad-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="666ad-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="666ad-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="666ad-140">INPUTS</span></span>

### <span data-ttu-id="666ad-141">Microsoft. Azure. commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="666ad-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="666ad-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="666ad-142">OUTPUTS</span></span>

### <span data-ttu-id="666ad-143">Microsoft. Azure. commands. reservations. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="666ad-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="666ad-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="666ad-144">NOTES</span></span>

## <span data-ttu-id="666ad-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="666ad-145">RELATED LINKS</span></span>
