---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainersastoken
schema: 2.0.0
ms.openlocfilehash: 3fa5a642bd5d8c53b81422f54fdb2c133304cc03
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931570"
---
# <span data-ttu-id="f85b8-101">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="f85b8-101">New-AzureStorageContainerSASToken</span></span>

## <span data-ttu-id="f85b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f85b8-102">SYNOPSIS</span></span>
<span data-ttu-id="f85b8-103">Skapar en SAS-token för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="f85b8-103">Generates an SAS token for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f85b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f85b8-104">SYNTAX</span></span>

### <span data-ttu-id="f85b8-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="f85b8-105">SasPolicy</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f85b8-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="f85b8-106">SasPermission</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f85b8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f85b8-107">DESCRIPTION</span></span>
<span data-ttu-id="f85b8-108">**New-AzureStorageContainerSASToken-** cmdleten genererar en SAS-token (Shared Access signatur) för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="f85b8-108">The **New-AzureStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="f85b8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f85b8-109">EXAMPLES</span></span>

### <span data-ttu-id="f85b8-110">Exempel 1: generera en SAS-token för behållare med fullständig behörighet för container</span><span class="sxs-lookup"><span data-stu-id="f85b8-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="f85b8-111">I det här exemplet skapas en SAS-token för behållare med fullständig behörighet för behållaren.</span><span class="sxs-lookup"><span data-stu-id="f85b8-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="f85b8-112">Exempel 2: generera en SAS-token med flera behållare per pipeline</span><span class="sxs-lookup"><span data-stu-id="f85b8-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container test* | New-AzureStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="f85b8-113">I det här exemplet skapas SAS-token med flera behållare med hjälp av pipeline.</span><span class="sxs-lookup"><span data-stu-id="f85b8-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="f85b8-114">Exempel 3: skapa SAS-token för behållare med delad åtkomst policy</span><span class="sxs-lookup"><span data-stu-id="f85b8-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="f85b8-115">I det här exemplet skapas en SAS-token för behållare med delad åtkomst policy.</span><span class="sxs-lookup"><span data-stu-id="f85b8-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="f85b8-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f85b8-116">PARAMETERS</span></span>

### <span data-ttu-id="f85b8-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="f85b8-117">-Context</span></span>
<span data-ttu-id="f85b8-118">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="f85b8-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f85b8-119">Du kan skapa det med hjälp av New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f85b8-119">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f85b8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f85b8-120">-DefaultProfile</span></span>
<span data-ttu-id="f85b8-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f85b8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85b8-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f85b8-122">-ExpiryTime</span></span>
<span data-ttu-id="f85b8-123">Anger den tid då den delade åtkomst-signaturen blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="f85b8-123">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="f85b8-124">Om användaren anger start tiden men inte utgångs tiden, anges start tiden plus en timme.</span><span class="sxs-lookup"><span data-stu-id="f85b8-124">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="f85b8-125">Om varken start tiden eller utgångs tiden har angetts anges den aktuella tiden plus en timme.</span><span class="sxs-lookup"><span data-stu-id="f85b8-125">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85b8-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="f85b8-126">-FullUri</span></span>
<span data-ttu-id="f85b8-127">Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="f85b8-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="f85b8-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="f85b8-128">-IPAddressOrRange</span></span>
<span data-ttu-id="f85b8-129">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="f85b8-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="f85b8-130">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="f85b8-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="f85b8-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="f85b8-131">-Name</span></span>
<span data-ttu-id="f85b8-132">Anger ett namn på en Azure-lagringsenhet.</span><span class="sxs-lookup"><span data-stu-id="f85b8-132">Specifies an Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f85b8-133">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="f85b8-133">-Permission</span></span>
<span data-ttu-id="f85b8-134">Anger behörigheter för en lagrings behållare.</span><span class="sxs-lookup"><span data-stu-id="f85b8-134">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="f85b8-135">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="f85b8-135">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85b8-136">-Princip</span><span class="sxs-lookup"><span data-stu-id="f85b8-136">-Policy</span></span>
<span data-ttu-id="f85b8-137">Anger en åtkomst policy för Azure.</span><span class="sxs-lookup"><span data-stu-id="f85b8-137">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85b8-138">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="f85b8-138">-Protocol</span></span>
<span data-ttu-id="f85b8-139">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="f85b8-139">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="f85b8-140">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f85b8-140">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="f85b8-141">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="f85b8-141">HttpsOnly</span></span>
* <span data-ttu-id="f85b8-142">HttpsOrHttp standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="f85b8-142">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85b8-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f85b8-143">-StartTime</span></span>
<span data-ttu-id="f85b8-144">Anger den tid då den delade Access-signaturen blir giltig.</span><span class="sxs-lookup"><span data-stu-id="f85b8-144">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85b8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f85b8-145">CommonParameters</span></span>
<span data-ttu-id="f85b8-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f85b8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f85b8-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f85b8-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f85b8-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f85b8-148">INPUTS</span></span>

### <span data-ttu-id="f85b8-149">System. String</span><span class="sxs-lookup"><span data-stu-id="f85b8-149">System.String</span></span>

### <span data-ttu-id="f85b8-150">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f85b8-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f85b8-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f85b8-151">OUTPUTS</span></span>

### <span data-ttu-id="f85b8-152">System. String</span><span class="sxs-lookup"><span data-stu-id="f85b8-152">System.String</span></span>

## <span data-ttu-id="f85b8-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f85b8-153">NOTES</span></span>

## <span data-ttu-id="f85b8-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f85b8-154">RELATED LINKS</span></span>

[<span data-ttu-id="f85b8-155">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f85b8-155">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)