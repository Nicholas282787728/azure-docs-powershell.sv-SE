---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 368ae4ad814c9414ea211ea6e44c2d3fbda005f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521926"
---
# <span data-ttu-id="1d18c-101">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="1d18c-101">Get-AzSupportTicket</span></span>

## <span data-ttu-id="1d18c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d18c-102">SYNOPSIS</span></span>
<span data-ttu-id="1d18c-103">Få support biljetter.</span><span class="sxs-lookup"><span data-stu-id="1d18c-103">Get support tickets.</span></span>

## <span data-ttu-id="1d18c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d18c-104">SYNTAX</span></span>

### <span data-ttu-id="1d18c-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1d18c-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1d18c-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d18c-106">GetByNameParameterSet</span></span>
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="1d18c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d18c-107">DESCRIPTION</span></span>
<span data-ttu-id="1d18c-108">Hämtar listan med support biljetter.</span><span class="sxs-lookup"><span data-stu-id="1d18c-108">Gets the list of support tickets.</span></span> <span data-ttu-id="1d18c-109">Då hämtas alla support biljetter om du inte anger några parametrar.</span><span class="sxs-lookup"><span data-stu-id="1d18c-109">It will retrieve all the support tickets if you do not specify any parameters.</span></span> <span data-ttu-id="1d18c-110">Du kan också filtrera support biljetter efter status eller CreatedDate med hjälp av parametern filter.</span><span class="sxs-lookup"><span data-stu-id="1d18c-110">You can also filter the support tickets by Status or CreatedDate using the Filter parameter.</span></span> <span data-ttu-id="1d18c-111">Här är några exempel på filter värden som du kan ange.</span><span class="sxs-lookup"><span data-stu-id="1d18c-111">Here are some examples of filter values that you can specify.</span></span>

| <span data-ttu-id="1d18c-112">Ovanligt</span><span class="sxs-lookup"><span data-stu-id="1d18c-112">Scenario</span></span>                                                         | <span data-ttu-id="1d18c-113">Filtrera</span><span class="sxs-lookup"><span data-stu-id="1d18c-113">Filter</span></span>                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="1d18c-114">Få biljetter som är öppna</span><span class="sxs-lookup"><span data-stu-id="1d18c-114">Get tickets that are in open state</span></span>                               | <span data-ttu-id="1d18c-115">"Status EQ" Open "</span><span class="sxs-lookup"><span data-stu-id="1d18c-115">"Status eq 'Open'"</span></span>                               |
| <span data-ttu-id="1d18c-116">Få biljetter som är i stängt tillstånd</span><span class="sxs-lookup"><span data-stu-id="1d18c-116">Get tickets that are in closed state</span></span>                             | <span data-ttu-id="1d18c-117">"Status EQ" stängd "</span><span class="sxs-lookup"><span data-stu-id="1d18c-117">"Status eq 'Closed'"</span></span>                             |
| <span data-ttu-id="1d18c-118">Få biljetter som skapades på eller efter den 20 dec, 2019</span><span class="sxs-lookup"><span data-stu-id="1d18c-118">Get tickets that were created on or after 20th Dec, 2019</span></span>         | <span data-ttu-id="1d18c-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="1d18c-119">"CreatedDate ge 2019-12-20"</span></span>                      |
| <span data-ttu-id="1d18c-120">Få biljetter som har skapats efter den 20 dec 2019</span><span class="sxs-lookup"><span data-stu-id="1d18c-120">Get tickets that were created after 20th Dec, 2019</span></span>               | <span data-ttu-id="1d18c-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="1d18c-121">"CreatedDate gt 2019-12-20"</span></span>                      |
| <span data-ttu-id="1d18c-122">Hämtar biljetter som skapats efter den 20 dec, 2019 som är i öppet läge</span><span class="sxs-lookup"><span data-stu-id="1d18c-122">Gets tickets created after 20th Dec, 2019 that are in open state</span></span> | <span data-ttu-id="1d18c-123">"CreatedDate gt 2019-12-20 och status EQ" Open "</span><span class="sxs-lookup"><span data-stu-id="1d18c-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span></span> |


<span data-ttu-id="1d18c-124">Denna cmdlet har stöd för växling via första och hoppa över parametrar.</span><span class="sxs-lookup"><span data-stu-id="1d18c-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="1d18c-125">Du kan också hämta ett enskilt support ärende genom att ange biljett namnet.</span><span class="sxs-lookup"><span data-stu-id="1d18c-125">You can also retrieve a single support ticket by specifying the ticket name.</span></span> 

## <span data-ttu-id="1d18c-126">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d18c-126">EXAMPLES</span></span>

### <span data-ttu-id="1d18c-127">Exempel 1: få första 2 biljetterna</span><span class="sxs-lookup"><span data-stu-id="1d18c-127">Example 1: Get first 2 tickets</span></span>
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="1d18c-128">Exempel 2: få första två biljetter efter att ha hoppat av de första två</span><span class="sxs-lookup"><span data-stu-id="1d18c-128">Example 2: Get first 2 tickets after skipping the first 2</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="1d18c-129">Exempel 3: skaffa ett support ärende utifrån namn</span><span class="sxs-lookup"><span data-stu-id="1d18c-129">Example 3: Get a support ticket by name</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="1d18c-130">Exempel 4: Hämta första 2 support biljetter filtrerade efter status</span><span class="sxs-lookup"><span data-stu-id="1d18c-130">Example 4: Get first 2 support tickets filtered by status</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="1d18c-131">Exempel 5: få alla support biljetter som är öppna och skapade efter dec den 2019</span><span class="sxs-lookup"><span data-stu-id="1d18c-131">Example 5: Get all support tickets that are in Open state and created after Dec 20th, 2019</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="1d18c-132">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d18c-132">PARAMETERS</span></span>

### <span data-ttu-id="1d18c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d18c-133">-DefaultProfile</span></span>
<span data-ttu-id="1d18c-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1d18c-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d18c-135">-Filter</span><span class="sxs-lookup"><span data-stu-id="1d18c-135">-Filter</span></span>
<span data-ttu-id="1d18c-136">Filter som ska tillämpas på resultatet av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d18c-136">Filter to be applied to the results of this cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d18c-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="1d18c-137">-Name</span></span>
<span data-ttu-id="1d18c-138">Namnet på det support ärende som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="1d18c-138">Name of support ticket that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d18c-139">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="1d18c-139">-IncludeTotalCount</span></span>
<span data-ttu-id="1d18c-140">Rapporterar totalt antal objekt i data uppsättningen (ett heltal) följt av de markerade objekten.</span><span class="sxs-lookup"><span data-stu-id="1d18c-140">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="1d18c-141">Om cmdleten inte kan bestämma det totala antalet visar den "okänt antal".</span><span class="sxs-lookup"><span data-stu-id="1d18c-141">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="1d18c-142">Heltalet har en egenskap för exakthet som anger tillförlitligheten hos det totala värdet.</span><span class="sxs-lookup"><span data-stu-id="1d18c-142">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="1d18c-143">Värdet för precisions intervall från 0,0 till 1,0 där 0,0 innebär att cmdleten inte kan räkna antalet objekt, ger 1,0 att antalet är exakt och ett värde mellan 0,0 och 1,0 tyder på en allt tillförlitlig uppskattning.</span><span class="sxs-lookup"><span data-stu-id="1d18c-143">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="1d18c-144">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="1d18c-144">-Skip</span></span>
<span data-ttu-id="1d18c-145">Ignorerar angivet antal objekt och hämtar sedan återstående objekt.</span><span class="sxs-lookup"><span data-stu-id="1d18c-145">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="1d18c-146">Ange antalet objekt som ska hoppas över.</span><span class="sxs-lookup"><span data-stu-id="1d18c-146">Enter the number of objects to skip.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d18c-147">-Först</span><span class="sxs-lookup"><span data-stu-id="1d18c-147">-First</span></span>
<span data-ttu-id="1d18c-148">Hämtar bara angivet antal objekt.</span><span class="sxs-lookup"><span data-stu-id="1d18c-148">Gets only the specified number of objects.</span></span>
<span data-ttu-id="1d18c-149">Ange antalet objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="1d18c-149">Enter the number of objects to get.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d18c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d18c-150">CommonParameters</span></span>
<span data-ttu-id="1d18c-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d18c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d18c-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d18c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d18c-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d18c-153">INPUTS</span></span>

### <span data-ttu-id="1d18c-154">Ingen</span><span class="sxs-lookup"><span data-stu-id="1d18c-154">None</span></span>

## <span data-ttu-id="1d18c-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d18c-155">OUTPUTS</span></span>

### <span data-ttu-id="1d18c-156">Microsoft. Azure. commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="1d18c-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="1d18c-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d18c-157">NOTES</span></span>

## <span data-ttu-id="1d18c-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d18c-158">RELATED LINKS</span></span>
