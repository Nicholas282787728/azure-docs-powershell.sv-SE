---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 07a8747f94f9c1fb93bbff06ce855363088a67a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260898"
---
# <span data-ttu-id="d31c1-101">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="d31c1-101">Get-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="d31c1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d31c1-102">SYNOPSIS</span></span>
<span data-ttu-id="d31c1-103">Få support biljett kommunikation.</span><span class="sxs-lookup"><span data-stu-id="d31c1-103">Get support ticket communications.</span></span>

## <span data-ttu-id="d31c1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d31c1-104">SYNTAX</span></span>

### <span data-ttu-id="d31c1-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d31c1-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### <span data-ttu-id="d31c1-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d31c1-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="d31c1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d31c1-107">DESCRIPTION</span></span>
<span data-ttu-id="d31c1-108">Får ett support ärende.</span><span class="sxs-lookup"><span data-stu-id="d31c1-108">Gets communications for a support ticket.</span></span> <span data-ttu-id="d31c1-109">Då hämtas all kommunikation för en biljett om du inte anger några andra parametrar.</span><span class="sxs-lookup"><span data-stu-id="d31c1-109">It will retrieve all the communications for a ticket if you do not specify any other parameters.</span></span> <span data-ttu-id="d31c1-110">Du kan också filtrera kommunikationen genom att CreatedDate eller CommunicationType med parametern filter.</span><span class="sxs-lookup"><span data-stu-id="d31c1-110">You can also filter the communications by CreatedDate or CommunicationType using the Filter parameter.</span></span> <span data-ttu-id="d31c1-111">Här är några exempel på filter värden som du kan ange.</span><span class="sxs-lookup"><span data-stu-id="d31c1-111">Here are some examples of filter values that you can specify.</span></span>


| <span data-ttu-id="d31c1-112">Ovanligt</span><span class="sxs-lookup"><span data-stu-id="d31c1-112">Scenario</span></span>                                                        | <span data-ttu-id="d31c1-113">Filtrera</span><span class="sxs-lookup"><span data-stu-id="d31c1-113">Filter</span></span>                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d31c1-114">Få webb kommunikation</span><span class="sxs-lookup"><span data-stu-id="d31c1-114">Get Web communications</span></span>                                          | <span data-ttu-id="d31c1-115">"CommunicationType EQ"-webben "</span><span class="sxs-lookup"><span data-stu-id="d31c1-115">"CommunicationType eq 'Web'"</span></span>                               |
| <span data-ttu-id="d31c1-116">Få telefon kommunikation</span><span class="sxs-lookup"><span data-stu-id="d31c1-116">Get Phone communications</span></span>                                        | <span data-ttu-id="d31c1-117">"CommunicationType EQ"-telefon "</span><span class="sxs-lookup"><span data-stu-id="d31c1-117">"CommunicationType eq 'Phone'"</span></span>                             |
| <span data-ttu-id="d31c1-118">Skaffa kommunikation som skapades på eller efter den 20 dec, 2019</span><span class="sxs-lookup"><span data-stu-id="d31c1-118">Get communications that were created on or after 20th Dec, 2019</span></span> | <span data-ttu-id="d31c1-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="d31c1-119">"CreatedDate ge 2019-12-20"</span></span>                                |
| <span data-ttu-id="d31c1-120">Få meddelanden som har skapats efter den 20 dec 2019</span><span class="sxs-lookup"><span data-stu-id="d31c1-120">Get communications that were created after 20th Dec, 2019</span></span>       | <span data-ttu-id="d31c1-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="d31c1-121">"CreatedDate gt 2019-12-20"</span></span>                                |
| <span data-ttu-id="d31c1-122">Får webb kommunikation skapad efter den 20 dec, 2019</span><span class="sxs-lookup"><span data-stu-id="d31c1-122">Gets Web communications created after 20th Dec, 2019</span></span>            | <span data-ttu-id="d31c1-123">"CreatedDate gt 2019-12-20 och CommunicationType EQ" webben "</span><span class="sxs-lookup"><span data-stu-id="d31c1-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span></span> |


<span data-ttu-id="d31c1-124">Denna cmdlet har stöd för växling via första och hoppa över parametrar.</span><span class="sxs-lookup"><span data-stu-id="d31c1-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="d31c1-125">Du kan också hämta en enda support biljetts kommunikation genom att ange namnet på kommunikationen.</span><span class="sxs-lookup"><span data-stu-id="d31c1-125">You can also retrieve a single support ticket communication by specifying the communication name.</span></span> 

## <span data-ttu-id="d31c1-126">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d31c1-126">EXAMPLES</span></span>

### <span data-ttu-id="d31c1-127">Exempel 1: Hämta all kommunikation för ett support ärende</span><span class="sxs-lookup"><span data-stu-id="d31c1-127">Example 1: Retrieve all communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### <span data-ttu-id="d31c1-128">Exempel 2: Hämta en enda kommunikation via namnet för ett support ärende</span><span class="sxs-lookup"><span data-stu-id="d31c1-128">Example 2: Retrieve a single communication by it's name for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### <span data-ttu-id="d31c1-129">Exempel 3: Hämta första 2-kommunikationen för ett support ärende</span><span class="sxs-lookup"><span data-stu-id="d31c1-129">Example 3: Retrieve first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="d31c1-130">Exempel 4: Hämta nästa 2 kommunikation efter att du hoppat över den första 2 kommunikationen för ett support ärende</span><span class="sxs-lookup"><span data-stu-id="d31c1-130">Example 4: Retrieve next 2 communications after skipping first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="d31c1-131">Exempel 5: Hämta all webbkommunikation för ett support ärende</span><span class="sxs-lookup"><span data-stu-id="d31c1-131">Example 5: Retrieve all Web communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="d31c1-132">Exempel 6: Hämta all kommunikation som skapades på eller efter den 20 december 2019 för ett support ärende</span><span class="sxs-lookup"><span data-stu-id="d31c1-132">Example 6: Retrieve all communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="d31c1-133">Exempel 7: Hämta alla webb kommunikationer som skapats på eller efter den 20 december 2019 för ett support ärende</span><span class="sxs-lookup"><span data-stu-id="d31c1-133">Example 7: Retrieve all Web communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="d31c1-134">Exempel 8: Hämta all kommunikation för ett support ärende efter ledning-support</span><span class="sxs-lookup"><span data-stu-id="d31c1-134">Example 8: Retrieve all communications for a support ticket by piping support ticket object</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

## <span data-ttu-id="d31c1-135">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d31c1-135">PARAMETERS</span></span>

### <span data-ttu-id="d31c1-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d31c1-136">-DefaultProfile</span></span>
<span data-ttu-id="d31c1-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d31c1-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d31c1-138">-Filter</span><span class="sxs-lookup"><span data-stu-id="d31c1-138">-Filter</span></span>
<span data-ttu-id="d31c1-139">Filter som ska tillämpas på resultatet av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d31c1-139">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="d31c1-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="d31c1-140">-Name</span></span>
<span data-ttu-id="d31c1-141">Kommunikations namn.</span><span class="sxs-lookup"><span data-stu-id="d31c1-141">Communication name.</span></span>

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

### <span data-ttu-id="d31c1-142">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="d31c1-142">-SupportTicketName</span></span>
<span data-ttu-id="d31c1-143">Namn på support ärende.</span><span class="sxs-lookup"><span data-stu-id="d31c1-143">Support ticket name.</span></span>

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

### <span data-ttu-id="d31c1-144">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="d31c1-144">-SupportTicketObject</span></span>
<span data-ttu-id="d31c1-145">Objekt för support biljetter.</span><span class="sxs-lookup"><span data-stu-id="d31c1-145">Support ticket object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d31c1-146">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="d31c1-146">-IncludeTotalCount</span></span>
<span data-ttu-id="d31c1-147">Rapporterar totalt antal objekt i data uppsättningen (ett heltal) följt av de markerade objekten.</span><span class="sxs-lookup"><span data-stu-id="d31c1-147">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="d31c1-148">Om cmdleten inte kan bestämma det totala antalet visar den "okänt antal".</span><span class="sxs-lookup"><span data-stu-id="d31c1-148">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="d31c1-149">Heltalet har en egenskap för exakthet som anger tillförlitligheten hos det totala värdet.</span><span class="sxs-lookup"><span data-stu-id="d31c1-149">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="d31c1-150">Värdet för precisions intervall från 0,0 till 1,0 där 0,0 innebär att cmdleten inte kan räkna antalet objekt, ger 1,0 att antalet är exakt och ett värde mellan 0,0 och 1,0 tyder på en allt tillförlitlig uppskattning.</span><span class="sxs-lookup"><span data-stu-id="d31c1-150">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="d31c1-151">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="d31c1-151">-Skip</span></span>
<span data-ttu-id="d31c1-152">Ignorerar angivet antal objekt och hämtar sedan återstående objekt.</span><span class="sxs-lookup"><span data-stu-id="d31c1-152">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="d31c1-153">Ange antalet objekt som ska hoppas över.</span><span class="sxs-lookup"><span data-stu-id="d31c1-153">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="d31c1-154">-Först</span><span class="sxs-lookup"><span data-stu-id="d31c1-154">-First</span></span>
<span data-ttu-id="d31c1-155">Hämtar bara angivet antal objekt.</span><span class="sxs-lookup"><span data-stu-id="d31c1-155">Gets only the specified number of objects.</span></span>
<span data-ttu-id="d31c1-156">Ange antalet objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="d31c1-156">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="d31c1-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d31c1-157">CommonParameters</span></span>
<span data-ttu-id="d31c1-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d31c1-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d31c1-159">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d31c1-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d31c1-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d31c1-160">INPUTS</span></span>

### <span data-ttu-id="d31c1-161">Microsoft. Azure. commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="d31c1-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="d31c1-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d31c1-162">OUTPUTS</span></span>

### <span data-ttu-id="d31c1-163">Microsoft. Azure. commands. support. Models. PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="d31c1-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="d31c1-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d31c1-164">NOTES</span></span>

## <span data-ttu-id="d31c1-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d31c1-165">RELATED LINKS</span></span>
