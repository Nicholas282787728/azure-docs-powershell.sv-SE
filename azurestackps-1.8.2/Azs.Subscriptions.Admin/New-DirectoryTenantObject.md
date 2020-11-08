---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20b70e2eeb1aa2d98f595dfe7bbe3075174c1f64
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100080"
---
# <span data-ttu-id="f665d-101">New-DirectoryTenantObject</span><span class="sxs-lookup"><span data-stu-id="f665d-101">New-DirectoryTenantObject</span></span>

## <span data-ttu-id="f665d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f665d-102">SYNOPSIS</span></span>
<span data-ttu-id="f665d-103">Katalog klient organisation.</span><span class="sxs-lookup"><span data-stu-id="f665d-103">Directory tenant.</span></span>

## <span data-ttu-id="f665d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f665d-104">SYNTAX</span></span>

```
New-DirectoryTenantObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-Name] <String>]
 [[-TenantId] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="f665d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f665d-105">DESCRIPTION</span></span>
<span data-ttu-id="f665d-106">Katalog klient organisation.</span><span class="sxs-lookup"><span data-stu-id="f665d-106">Directory tenant.</span></span>

## <span data-ttu-id="f665d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f665d-107">EXAMPLES</span></span>

### <span data-ttu-id="f665d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f665d-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="f665d-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="f665d-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="f665d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f665d-110">PARAMETERS</span></span>

### <span data-ttu-id="f665d-111">-ID</span><span class="sxs-lookup"><span data-stu-id="f665d-111">-Id</span></span>
<span data-ttu-id="f665d-112">URI för resursen.</span><span class="sxs-lookup"><span data-stu-id="f665d-112">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f665d-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="f665d-113">-Location</span></span>
<span data-ttu-id="f665d-114">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="f665d-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f665d-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="f665d-115">-Name</span></span>
<span data-ttu-id="f665d-116">Namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="f665d-116">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f665d-117">-Taggar</span><span class="sxs-lookup"><span data-stu-id="f665d-117">-Tags</span></span>
<span data-ttu-id="f665d-118">Lista över par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="f665d-118">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f665d-119">-TenantId</span><span class="sxs-lookup"><span data-stu-id="f665d-119">-TenantId</span></span>
<span data-ttu-id="f665d-120">Unik identifierare för klient organisation.</span><span class="sxs-lookup"><span data-stu-id="f665d-120">Tenant unique identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f665d-121">– Skriv</span><span class="sxs-lookup"><span data-stu-id="f665d-121">-Type</span></span>
<span data-ttu-id="f665d-122">Typ av resurs.</span><span class="sxs-lookup"><span data-stu-id="f665d-122">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f665d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f665d-123">CommonParameters</span></span>
<span data-ttu-id="f665d-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f665d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f665d-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f665d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f665d-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f665d-126">INPUTS</span></span>

## <span data-ttu-id="f665d-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f665d-127">OUTPUTS</span></span>

## <span data-ttu-id="f665d-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f665d-128">NOTES</span></span>

## <span data-ttu-id="f665d-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f665d-129">RELATED LINKS</span></span>

