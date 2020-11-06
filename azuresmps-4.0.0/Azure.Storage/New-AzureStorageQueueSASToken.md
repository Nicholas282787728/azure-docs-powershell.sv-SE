---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac818fd403df9b159671f5889e068bda82a086d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572012"
---
# <span data-ttu-id="e2a2e-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="e2a2e-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="e2a2e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2a2e-102">SYNOPSIS</span></span>
<span data-ttu-id="e2a2e-103">Skapar ett signatur-token för delad åtkomst för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="e2a2e-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="e2a2e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2a2e-104">SYNTAX</span></span>

### <span data-ttu-id="e2a2e-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="e2a2e-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="e2a2e-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="e2a2e-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="e2a2e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2a2e-107">DESCRIPTION</span></span>
<span data-ttu-id="e2a2e-108">Cmdleten **New-AzureStorageQueueSASToken** för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="e2a2e-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="e2a2e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2a2e-109">EXAMPLES</span></span>

### <span data-ttu-id="e2a2e-110">Exempel 1: generera en SAS-token i kö med fullständig behörighet</span><span class="sxs-lookup"><span data-stu-id="e2a2e-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="e2a2e-111">I det här exemplet skapas en SAS-token för kön med fullständig behörighet.</span><span class="sxs-lookup"><span data-stu-id="e2a2e-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="e2a2e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2a2e-112">PARAMETERS</span></span>

### <span data-ttu-id="e2a2e-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="e2a2e-113">-Context</span></span>
<span data-ttu-id="e2a2e-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="e2a2e-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="e2a2e-115">Du kan skapa den via New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2a2e-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a2e-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e2a2e-116">-ExpiryTime</span></span>
<span data-ttu-id="e2a2e-117">Anger när signaturen för delad åtkomst inte längre är giltig.</span><span class="sxs-lookup"><span data-stu-id="e2a2e-117">Specifies when the shared access signature is no longer valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a2e-118">-FullUri</span><span class="sxs-lookup"><span data-stu-id="e2a2e-118">-FullUri</span></span>
<span data-ttu-id="e2a2e-119">Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="e2a2e-119">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a2e-120">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e2a2e-120">-IPAddressOrRange</span></span>
<span data-ttu-id="e2a2e-121">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="e2a2e-121">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="e2a2e-122">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="e2a2e-122">The range is inclusive.</span></span>

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

### <span data-ttu-id="e2a2e-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="e2a2e-123">-Name</span></span>
<span data-ttu-id="e2a2e-124">Anger ett namn på en Azure-lagringsprovider.</span><span class="sxs-lookup"><span data-stu-id="e2a2e-124">Specifies an Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a2e-125">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="e2a2e-125">-Permission</span></span>
<span data-ttu-id="e2a2e-126">Anger behörigheter för en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="e2a2e-126">Specifies permissions for a storage queue.</span></span>

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a2e-127">-Princip</span><span class="sxs-lookup"><span data-stu-id="e2a2e-127">-Policy</span></span>
<span data-ttu-id="e2a2e-128">Anger en åtkomst policy för Azure.</span><span class="sxs-lookup"><span data-stu-id="e2a2e-128">Specifies an Azure stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a2e-129">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="e2a2e-129">-Protocol</span></span>
<span data-ttu-id="e2a2e-130">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="e2a2e-130">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="e2a2e-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e2a2e-131">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="e2a2e-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="e2a2e-132">HttpsOnly</span></span>
* <span data-ttu-id="e2a2e-133">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="e2a2e-133">HttpsOrHttp</span></span>

<span data-ttu-id="e2a2e-134">Standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="e2a2e-134">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a2e-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e2a2e-135">-StartTime</span></span>
<span data-ttu-id="e2a2e-136">Anger när signaturen för delad åtkomst blir giltig.</span><span class="sxs-lookup"><span data-stu-id="e2a2e-136">Specifies when the shared access signature becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a2e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2a2e-137">CommonParameters</span></span>
<span data-ttu-id="e2a2e-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2a2e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2a2e-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2a2e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2a2e-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2a2e-140">INPUTS</span></span>

## <span data-ttu-id="e2a2e-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2a2e-141">OUTPUTS</span></span>

## <span data-ttu-id="e2a2e-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2a2e-142">NOTES</span></span>

## <span data-ttu-id="e2a2e-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2a2e-143">RELATED LINKS</span></span>

