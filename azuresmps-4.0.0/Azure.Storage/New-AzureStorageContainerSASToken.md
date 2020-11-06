---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: ''
schema: 2.0.0
ms.openlocfilehash: becdf63590b5c5abc5e7095b96e13586232311d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572332"
---
# <span data-ttu-id="2c796-101">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="2c796-101">New-AzureStorageContainerSASToken</span></span>

## <span data-ttu-id="2c796-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c796-102">SYNOPSIS</span></span>
<span data-ttu-id="2c796-103">Skapar en SAS-token för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="2c796-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="2c796-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c796-104">SYNTAX</span></span>

### <span data-ttu-id="2c796-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="2c796-105">SasPolicy</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="2c796-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="2c796-106">SasPermission</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="2c796-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c796-107">DESCRIPTION</span></span>
<span data-ttu-id="2c796-108">**New-AzureStorageContainerSASToken-** cmdleten genererar en SAS-token (Shared Access signatur) för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="2c796-108">The **New-AzureStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="2c796-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c796-109">EXAMPLES</span></span>

### <span data-ttu-id="2c796-110">Exempel 1: generera en SAS-token för behållare med fullständig behörighet för container</span><span class="sxs-lookup"><span data-stu-id="2c796-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="2c796-111">I det här exemplet skapas en SAS-token för behållare med fullständig behörighet för behållaren.</span><span class="sxs-lookup"><span data-stu-id="2c796-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="2c796-112">Exempel 2: generera en SAS-token med flera behållare per pipeline</span><span class="sxs-lookup"><span data-stu-id="2c796-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container test* | New-AzureStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="2c796-113">I det här exemplet skapas SAS-token med flera behållare med hjälp av pipeline.</span><span class="sxs-lookup"><span data-stu-id="2c796-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="2c796-114">Exempel 3: skapa SAS-token för behållare med delad åtkomst policy</span><span class="sxs-lookup"><span data-stu-id="2c796-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="2c796-115">I det här exemplet skapas en SAS-token för behållare med delad åtkomst policy.</span><span class="sxs-lookup"><span data-stu-id="2c796-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="2c796-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c796-116">PARAMETERS</span></span>

### <span data-ttu-id="2c796-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2c796-117">-Context</span></span>
<span data-ttu-id="2c796-118">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="2c796-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2c796-119">Du kan skapa det med hjälp av New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c796-119">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2c796-120">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2c796-120">-ExpiryTime</span></span>
<span data-ttu-id="2c796-121">Anger den tid då den delade åtkomst-signaturen blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="2c796-121">Specifies the time at which the shared access signature becomes invalid.</span></span>

<span data-ttu-id="2c796-122">Om användaren anger start tiden men inte utgångs tiden, anges start tiden plus en timme.</span><span class="sxs-lookup"><span data-stu-id="2c796-122">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="2c796-123">Om varken start tiden eller utgångs tiden har angetts anges den aktuella tiden plus en timme.</span><span class="sxs-lookup"><span data-stu-id="2c796-123">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="2c796-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="2c796-124">-FullUri</span></span>
<span data-ttu-id="2c796-125">Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="2c796-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="2c796-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="2c796-126">-IPAddressOrRange</span></span>
<span data-ttu-id="2c796-127">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="2c796-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="2c796-128">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="2c796-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="2c796-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="2c796-129">-Name</span></span>
<span data-ttu-id="2c796-130">Anger ett namn på en Azure-lagringsenhet.</span><span class="sxs-lookup"><span data-stu-id="2c796-130">Specifies an Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c796-131">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="2c796-131">-Permission</span></span>
<span data-ttu-id="2c796-132">Anger behörigheter för en lagrings behållare.</span><span class="sxs-lookup"><span data-stu-id="2c796-132">Specifies permissions for a storage container.</span></span>

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

### <span data-ttu-id="2c796-133">-Princip</span><span class="sxs-lookup"><span data-stu-id="2c796-133">-Policy</span></span>
<span data-ttu-id="2c796-134">Anger en åtkomst policy för Azure.</span><span class="sxs-lookup"><span data-stu-id="2c796-134">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="2c796-135">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="2c796-135">-Protocol</span></span>
<span data-ttu-id="2c796-136">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="2c796-136">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="2c796-137">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2c796-137">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="2c796-138">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="2c796-138">HttpsOnly</span></span>
* <span data-ttu-id="2c796-139">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="2c796-139">HttpsOrHttp</span></span>

<span data-ttu-id="2c796-140">Standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="2c796-140">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="2c796-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2c796-141">-StartTime</span></span>
<span data-ttu-id="2c796-142">Anger den tid då den delade Access-signaturen blir giltig.</span><span class="sxs-lookup"><span data-stu-id="2c796-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="2c796-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c796-143">CommonParameters</span></span>
<span data-ttu-id="2c796-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c796-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c796-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c796-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c796-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c796-146">INPUTS</span></span>

## <span data-ttu-id="2c796-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c796-147">OUTPUTS</span></span>

## <span data-ttu-id="2c796-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c796-148">NOTES</span></span>

## <span data-ttu-id="2c796-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c796-149">RELATED LINKS</span></span>

[<span data-ttu-id="2c796-150">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="2c796-150">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)
