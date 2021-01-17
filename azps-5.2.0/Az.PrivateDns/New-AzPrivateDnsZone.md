---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
ms.openlocfilehash: 98830e2dbcfc115cd026c33782030bc40fa6763f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400323"
---
# <span data-ttu-id="41ed7-101">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="41ed7-101">New-AzPrivateDnsZone</span></span>

## <span data-ttu-id="41ed7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="41ed7-103">Skapar en ny privat DNS-zon.</span><span class="sxs-lookup"><span data-stu-id="41ed7-103">Creates a new private DNS zone.</span></span>

## <span data-ttu-id="41ed7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41ed7-104">SYNTAX</span></span>

```
New-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41ed7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41ed7-105">DESCRIPTION</span></span>
<span data-ttu-id="41ed7-106">Cmdleten **New-AzPrivateDnsZone** skapar en ny DNS-zon (Private Domain Name System) i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="41ed7-106">The **New-AzPrivateDnsZone** cmdlet creates a new private Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="41ed7-107">Du måste ange ett unikt namn för en privat DNS-zon för parametern *namn* så returnerar cmdleten ett fel.</span><span class="sxs-lookup"><span data-stu-id="41ed7-107">You must specify a unique private DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="41ed7-108">När zonen har skapats kan du använda New-AzPrivateDnsRecordSet cmdlet för att skapa post uppsättningar i zonen.</span><span class="sxs-lookup"><span data-stu-id="41ed7-108">After the zone is created, use the New-AzPrivateDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="41ed7-109">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="41ed7-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="41ed7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41ed7-110">EXAMPLES</span></span>

### <span data-ttu-id="41ed7-111">Exempel 1: skapa en privat DNS-zon</span><span class="sxs-lookup"><span data-stu-id="41ed7-111">Example 1: Create a Private DNS zone</span></span>
```
PS C:\>$Zone = New-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"


This command creates a new private DNS zone named myzone.com in the specified resource group, and then
stores it in the $Zone variable. $Zone object looks something like this,

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="41ed7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41ed7-112">PARAMETERS</span></span>

### <span data-ttu-id="41ed7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41ed7-113">-DefaultProfile</span></span>
<span data-ttu-id="41ed7-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="41ed7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41ed7-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="41ed7-115">-Name</span></span>
<span data-ttu-id="41ed7-116">Anger namnet på den privata DNS-zon som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="41ed7-116">Specifies the name of the private DNS zone to create.</span></span>

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

### <span data-ttu-id="41ed7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41ed7-117">-ResourceGroupName</span></span>
<span data-ttu-id="41ed7-118">Anger den resurs grupp som du vill skapa zonen i.</span><span class="sxs-lookup"><span data-stu-id="41ed7-118">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="41ed7-119">-Tagg</span><span class="sxs-lookup"><span data-stu-id="41ed7-119">-Tag</span></span>
<span data-ttu-id="41ed7-120">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="41ed7-120">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41ed7-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="41ed7-121">-Confirm</span></span>
<span data-ttu-id="41ed7-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="41ed7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41ed7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41ed7-123">-WhatIf</span></span>
<span data-ttu-id="41ed7-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="41ed7-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41ed7-125">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="41ed7-125">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41ed7-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="41ed7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41ed7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41ed7-127">CommonParameters</span></span>
<span data-ttu-id="41ed7-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41ed7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41ed7-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41ed7-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41ed7-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41ed7-130">INPUTS</span></span>

### <span data-ttu-id="41ed7-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="41ed7-131">None</span></span>

## <span data-ttu-id="41ed7-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41ed7-132">OUTPUTS</span></span>

### <span data-ttu-id="41ed7-133">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="41ed7-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="41ed7-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41ed7-134">NOTES</span></span>

## <span data-ttu-id="41ed7-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41ed7-135">RELATED LINKS</span></span>

[<span data-ttu-id="41ed7-136">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="41ed7-136">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="41ed7-137">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="41ed7-137">New-AzPrivateDnsRecordSet</span></span>](./New-AzPrivateDnsRecordSet.md)

[<span data-ttu-id="41ed7-138">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="41ed7-138">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)
