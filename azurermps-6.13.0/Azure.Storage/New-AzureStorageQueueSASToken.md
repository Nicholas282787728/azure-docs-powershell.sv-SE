---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
ms.openlocfilehash: 337dcb1718cf48488115e38052c0fdfed73edc3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579199"
---
# <span data-ttu-id="ec1ef-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="ec1ef-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="ec1ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ec1ef-102">SYNOPSIS</span></span>
<span data-ttu-id="ec1ef-103">Skapar ett signatur-token för delad åtkomst för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-103">Generates a shared access signature token for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec1ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ec1ef-104">SYNTAX</span></span>

### <span data-ttu-id="ec1ef-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="ec1ef-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec1ef-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="ec1ef-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec1ef-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ec1ef-107">DESCRIPTION</span></span>
<span data-ttu-id="ec1ef-108">Cmdleten **New-AzureStorageQueueSASToken** för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="ec1ef-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ec1ef-109">EXAMPLES</span></span>

### <span data-ttu-id="ec1ef-110">Exempel 1: generera en SAS-token i kö med fullständig behörighet</span><span class="sxs-lookup"><span data-stu-id="ec1ef-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="ec1ef-111">I det här exemplet skapas en SAS-token för kön med fullständig behörighet.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="ec1ef-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ec1ef-112">PARAMETERS</span></span>

### <span data-ttu-id="ec1ef-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ec1ef-113">-Context</span></span>
<span data-ttu-id="ec1ef-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ec1ef-115">Du kan skapa den via New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ec1ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec1ef-116">-DefaultProfile</span></span>
<span data-ttu-id="ec1ef-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec1ef-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ec1ef-118">-ExpiryTime</span></span>
<span data-ttu-id="ec1ef-119">Anger när signaturen för delad åtkomst inte längre är giltig.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="ec1ef-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="ec1ef-120">-FullUri</span></span>
<span data-ttu-id="ec1ef-121">Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="ec1ef-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ec1ef-122">-IPAddressOrRange</span></span>
<span data-ttu-id="ec1ef-123">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="ec1ef-124">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="ec1ef-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="ec1ef-125">-Name</span></span>
<span data-ttu-id="ec1ef-126">Anger ett namn på en Azure-lagringsprovider.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-126">Specifies an Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec1ef-127">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="ec1ef-127">-Permission</span></span>
<span data-ttu-id="ec1ef-128">Anger behörigheter för en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="ec1ef-129">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="ec1ef-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="ec1ef-130">-Princip</span><span class="sxs-lookup"><span data-stu-id="ec1ef-130">-Policy</span></span>
<span data-ttu-id="ec1ef-131">Anger en åtkomst policy för Azure.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-131">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="ec1ef-132">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="ec1ef-132">-Protocol</span></span>
<span data-ttu-id="ec1ef-133">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="ec1ef-134">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ec1ef-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="ec1ef-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="ec1ef-135">HttpsOnly</span></span>
* <span data-ttu-id="ec1ef-136">HttpsOrHttp standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="ec1ef-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ec1ef-137">-StartTime</span></span>
<span data-ttu-id="ec1ef-138">Anger när signaturen för delad åtkomst blir giltig.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="ec1ef-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec1ef-139">CommonParameters</span></span>
<span data-ttu-id="ec1ef-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec1ef-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec1ef-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec1ef-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec1ef-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ec1ef-142">INPUTS</span></span>

### <span data-ttu-id="ec1ef-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ec1ef-143">System.String</span></span>

### <span data-ttu-id="ec1ef-144">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ec1ef-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ec1ef-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ec1ef-145">OUTPUTS</span></span>

### <span data-ttu-id="ec1ef-146">System. String</span><span class="sxs-lookup"><span data-stu-id="ec1ef-146">System.String</span></span>

## <span data-ttu-id="ec1ef-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ec1ef-147">NOTES</span></span>

## <span data-ttu-id="ec1ef-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ec1ef-148">RELATED LINKS</span></span>
