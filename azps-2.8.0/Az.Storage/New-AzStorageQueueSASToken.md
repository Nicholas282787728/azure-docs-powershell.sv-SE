---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
ms.openlocfilehash: 2ae003eaa20ddcc42fa31ab14c64f78255140c29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919522"
---
# <span data-ttu-id="54402-101">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="54402-101">New-AzStorageQueueSASToken</span></span>

## <span data-ttu-id="54402-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54402-102">SYNOPSIS</span></span>
<span data-ttu-id="54402-103">Skapar ett signatur-token för delad åtkomst för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="54402-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="54402-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54402-104">SYNTAX</span></span>

### <span data-ttu-id="54402-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="54402-105">SasPolicy</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54402-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="54402-106">SasPermission</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54402-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54402-107">DESCRIPTION</span></span>
<span data-ttu-id="54402-108">Cmdleten **New-AzStorageQueueSASToken** för en Azure Storage-kö.</span><span class="sxs-lookup"><span data-stu-id="54402-108">The **New-AzStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="54402-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54402-109">EXAMPLES</span></span>

### <span data-ttu-id="54402-110">Exempel 1: generera en SAS-token i kö med fullständig behörighet</span><span class="sxs-lookup"><span data-stu-id="54402-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="54402-111">I det här exemplet skapas en SAS-token för kön med fullständig behörighet.</span><span class="sxs-lookup"><span data-stu-id="54402-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="54402-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54402-112">PARAMETERS</span></span>

### <span data-ttu-id="54402-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="54402-113">-Context</span></span>
<span data-ttu-id="54402-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="54402-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="54402-115">Du kan skapa den via New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54402-115">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="54402-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54402-116">-DefaultProfile</span></span>
<span data-ttu-id="54402-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54402-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54402-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="54402-118">-ExpiryTime</span></span>
<span data-ttu-id="54402-119">Anger när signaturen för delad åtkomst inte längre är giltig.</span><span class="sxs-lookup"><span data-stu-id="54402-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="54402-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="54402-120">-FullUri</span></span>
<span data-ttu-id="54402-121">Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="54402-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="54402-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="54402-122">-IPAddressOrRange</span></span>
<span data-ttu-id="54402-123">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="54402-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="54402-124">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="54402-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="54402-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="54402-125">-Name</span></span>
<span data-ttu-id="54402-126">Anger ett namn på en Azure-lagringsprovider.</span><span class="sxs-lookup"><span data-stu-id="54402-126">Specifies an Azure storage queue name.</span></span>

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

### <span data-ttu-id="54402-127">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="54402-127">-Permission</span></span>
<span data-ttu-id="54402-128">Anger behörigheter för en lagrings kö.</span><span class="sxs-lookup"><span data-stu-id="54402-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="54402-129">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="54402-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="54402-130">-Princip</span><span class="sxs-lookup"><span data-stu-id="54402-130">-Policy</span></span>
<span data-ttu-id="54402-131">Anger en åtkomst policy för Azure.</span><span class="sxs-lookup"><span data-stu-id="54402-131">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="54402-132">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="54402-132">-Protocol</span></span>
<span data-ttu-id="54402-133">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="54402-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="54402-134">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="54402-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="54402-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="54402-135">HttpsOnly</span></span>
* <span data-ttu-id="54402-136">HttpsOrHttp standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="54402-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54402-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="54402-137">-StartTime</span></span>
<span data-ttu-id="54402-138">Anger när signaturen för delad åtkomst blir giltig.</span><span class="sxs-lookup"><span data-stu-id="54402-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="54402-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54402-139">CommonParameters</span></span>
<span data-ttu-id="54402-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54402-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54402-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54402-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54402-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54402-142">INPUTS</span></span>

### <span data-ttu-id="54402-143">System. String</span><span class="sxs-lookup"><span data-stu-id="54402-143">System.String</span></span>

### <span data-ttu-id="54402-144">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="54402-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="54402-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54402-145">OUTPUTS</span></span>

### <span data-ttu-id="54402-146">System. String</span><span class="sxs-lookup"><span data-stu-id="54402-146">System.String</span></span>

## <span data-ttu-id="54402-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54402-147">NOTES</span></span>

## <span data-ttu-id="54402-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54402-148">RELATED LINKS</span></span>