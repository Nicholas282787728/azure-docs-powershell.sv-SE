---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 904305e383803e8ef672a82689794296f7c9b84d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586291"
---
# <span data-ttu-id="32ae8-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="32ae8-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="32ae8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="32ae8-102">SYNOPSIS</span></span>
<span data-ttu-id="32ae8-103">Skapar ett signatur-token för delad åtkomst för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="32ae8-103">Generates a shared access signature token for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32ae8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="32ae8-104">SYNTAX</span></span>

### <span data-ttu-id="32ae8-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="32ae8-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="32ae8-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="32ae8-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="32ae8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="32ae8-107">DESCRIPTION</span></span>
<span data-ttu-id="32ae8-108">Cmdleten **New-AzureStorageQueueSASToken** för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="32ae8-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="32ae8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="32ae8-109">EXAMPLES</span></span>

### <span data-ttu-id="32ae8-110">Exempel 1: generera en SAS-token i kö med fullständig behörighet</span><span class="sxs-lookup"><span data-stu-id="32ae8-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="32ae8-111">I det här exemplet skapas en SAS-token för kön med fullständig behörighet.</span><span class="sxs-lookup"><span data-stu-id="32ae8-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="32ae8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="32ae8-112">PARAMETERS</span></span>

### <span data-ttu-id="32ae8-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="32ae8-113">-Context</span></span>
<span data-ttu-id="32ae8-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="32ae8-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="32ae8-115">Du kan skapa den via New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32ae8-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="32ae8-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="32ae8-116">-ExpiryTime</span></span>
<span data-ttu-id="32ae8-117">Anger när signaturen för delad åtkomst inte längre är giltig.</span><span class="sxs-lookup"><span data-stu-id="32ae8-117">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="32ae8-118">-FullUri</span><span class="sxs-lookup"><span data-stu-id="32ae8-118">-FullUri</span></span>
<span data-ttu-id="32ae8-119">Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="32ae8-119">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="32ae8-120">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="32ae8-120">-IPAddressOrRange</span></span>
<span data-ttu-id="32ae8-121">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="32ae8-121">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="32ae8-122">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="32ae8-122">The range is inclusive.</span></span>

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

### <span data-ttu-id="32ae8-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="32ae8-123">-Name</span></span>
<span data-ttu-id="32ae8-124">Anger ett namn på en Azure-lagringsprovider.</span><span class="sxs-lookup"><span data-stu-id="32ae8-124">Specifies an Azure storage queue name.</span></span>

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

### <span data-ttu-id="32ae8-125">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="32ae8-125">-Permission</span></span>
<span data-ttu-id="32ae8-126">Anger behörigheter för en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="32ae8-126">Specifies permissions for a storage queue.</span></span>

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

### <span data-ttu-id="32ae8-127">-Princip</span><span class="sxs-lookup"><span data-stu-id="32ae8-127">-Policy</span></span>
<span data-ttu-id="32ae8-128">Anger en åtkomst policy för Azure.</span><span class="sxs-lookup"><span data-stu-id="32ae8-128">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="32ae8-129">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="32ae8-129">-Protocol</span></span>
<span data-ttu-id="32ae8-130">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="32ae8-130">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="32ae8-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="32ae8-131">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="32ae8-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="32ae8-132">HttpsOnly</span></span>
* <span data-ttu-id="32ae8-133">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="32ae8-133">HttpsOrHttp</span></span>

<span data-ttu-id="32ae8-134">Standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="32ae8-134">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="32ae8-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="32ae8-135">-StartTime</span></span>
<span data-ttu-id="32ae8-136">Anger när signaturen för delad åtkomst blir giltig.</span><span class="sxs-lookup"><span data-stu-id="32ae8-136">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="32ae8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32ae8-137">CommonParameters</span></span>
<span data-ttu-id="32ae8-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32ae8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32ae8-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32ae8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32ae8-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="32ae8-140">INPUTS</span></span>

### <span data-ttu-id="32ae8-141">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="32ae8-141">IStorageContext</span></span>

<span data-ttu-id="32ae8-142">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="32ae8-142">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="32ae8-143">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="32ae8-143">String</span></span>

<span data-ttu-id="32ae8-144">Parametern "name" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="32ae8-144">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="32ae8-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="32ae8-145">OUTPUTS</span></span>

### <span data-ttu-id="32ae8-146">System. String</span><span class="sxs-lookup"><span data-stu-id="32ae8-146">System.String</span></span>

## <span data-ttu-id="32ae8-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="32ae8-147">NOTES</span></span>

## <span data-ttu-id="32ae8-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="32ae8-148">RELATED LINKS</span></span>

