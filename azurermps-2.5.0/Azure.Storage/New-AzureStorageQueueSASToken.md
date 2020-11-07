---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuesastoken
schema: 2.0.0
ms.openlocfilehash: b002f518d63fb3ed4ed34d007f72b57e4db41ae5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930394"
---
# <span data-ttu-id="03046-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="03046-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="03046-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03046-102">SYNOPSIS</span></span>
<span data-ttu-id="03046-103">Skapar ett signatur-token för delad åtkomst för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="03046-103">Generates a shared access signature token for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03046-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03046-104">SYNTAX</span></span>

### <span data-ttu-id="03046-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="03046-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03046-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="03046-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03046-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03046-107">DESCRIPTION</span></span>
<span data-ttu-id="03046-108">Cmdleten **New-AzureStorageQueueSASToken** för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="03046-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="03046-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03046-109">EXAMPLES</span></span>

### <span data-ttu-id="03046-110">Exempel 1: generera en SAS-token i kö med fullständig behörighet</span><span class="sxs-lookup"><span data-stu-id="03046-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="03046-111">I det här exemplet skapas en SAS-token för kön med fullständig behörighet.</span><span class="sxs-lookup"><span data-stu-id="03046-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="03046-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03046-112">PARAMETERS</span></span>

### <span data-ttu-id="03046-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="03046-113">-Context</span></span>
<span data-ttu-id="03046-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="03046-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="03046-115">Du kan skapa den via New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03046-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="03046-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03046-116">-DefaultProfile</span></span>
<span data-ttu-id="03046-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="03046-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03046-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="03046-118">-ExpiryTime</span></span>
<span data-ttu-id="03046-119">Anger när signaturen för delad åtkomst inte längre är giltig.</span><span class="sxs-lookup"><span data-stu-id="03046-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="03046-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="03046-120">-FullUri</span></span>
<span data-ttu-id="03046-121">Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="03046-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="03046-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="03046-122">-IPAddressOrRange</span></span>
<span data-ttu-id="03046-123">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="03046-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="03046-124">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="03046-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="03046-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="03046-125">-Name</span></span>
<span data-ttu-id="03046-126">Anger ett namn på en Azure-lagringsprovider.</span><span class="sxs-lookup"><span data-stu-id="03046-126">Specifies an Azure storage queue name.</span></span>

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

### <span data-ttu-id="03046-127">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="03046-127">-Permission</span></span>
<span data-ttu-id="03046-128">Anger behörigheter för en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="03046-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="03046-129">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="03046-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="03046-130">-Princip</span><span class="sxs-lookup"><span data-stu-id="03046-130">-Policy</span></span>
<span data-ttu-id="03046-131">Anger en åtkomst policy för Azure.</span><span class="sxs-lookup"><span data-stu-id="03046-131">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="03046-132">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="03046-132">-Protocol</span></span>
<span data-ttu-id="03046-133">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="03046-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="03046-134">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="03046-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="03046-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="03046-135">HttpsOnly</span></span>
* <span data-ttu-id="03046-136">HttpsOrHttp standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="03046-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="03046-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="03046-137">-StartTime</span></span>
<span data-ttu-id="03046-138">Anger när signaturen för delad åtkomst blir giltig.</span><span class="sxs-lookup"><span data-stu-id="03046-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="03046-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03046-139">CommonParameters</span></span>
<span data-ttu-id="03046-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03046-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03046-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03046-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03046-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03046-142">INPUTS</span></span>

### <span data-ttu-id="03046-143">System. String</span><span class="sxs-lookup"><span data-stu-id="03046-143">System.String</span></span>

### <span data-ttu-id="03046-144">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="03046-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="03046-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03046-145">OUTPUTS</span></span>

### <span data-ttu-id="03046-146">System. String</span><span class="sxs-lookup"><span data-stu-id="03046-146">System.String</span></span>

## <span data-ttu-id="03046-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03046-147">NOTES</span></span>

## <span data-ttu-id="03046-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03046-148">RELATED LINKS</span></span>
