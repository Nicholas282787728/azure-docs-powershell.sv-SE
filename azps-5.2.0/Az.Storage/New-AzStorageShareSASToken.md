---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
ms.openlocfilehash: 8dbb6f79a61d388aec033030de471092fa16ba77
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388737"
---
# <span data-ttu-id="93c30-101">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="93c30-101">New-AzStorageShareSASToken</span></span>

## <span data-ttu-id="93c30-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93c30-102">SYNOPSIS</span></span>
<span data-ttu-id="93c30-103">Generera signatur för delad åtkomst för Azure Storage Share.</span><span class="sxs-lookup"><span data-stu-id="93c30-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="93c30-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93c30-104">SYNTAX</span></span>

### <span data-ttu-id="93c30-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="93c30-105">SasPolicy</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93c30-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="93c30-106">SasPermission</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93c30-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93c30-107">DESCRIPTION</span></span>
<span data-ttu-id="93c30-108">Cmdleten **New-AzStorageShareSASToken** skapar en signatur för delad åtkomst för en Azure-lagringsenhet.</span><span class="sxs-lookup"><span data-stu-id="93c30-108">The **New-AzStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="93c30-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93c30-109">EXAMPLES</span></span>

### <span data-ttu-id="93c30-110">Exempel 1: generera ett signatur-token för delad åtkomst för en resurs</span><span class="sxs-lookup"><span data-stu-id="93c30-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="93c30-111">Det här kommandot skapar ett signatur-token för delad åtkomst för resursen som heter ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="93c30-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="93c30-112">Exempel 2: generera flera signaturer med delad åtkomst med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="93c30-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "test" | New-AzStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="93c30-113">Det här kommandot får alla lagrings resurser som matchar prefixet.</span><span class="sxs-lookup"><span data-stu-id="93c30-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="93c30-114">Kommandot skickar dem till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="93c30-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="93c30-115">Den aktuella cmdleten skapar en delad åtkomsttoken för varje lagrings resurs som har de angivna behörigheterna.</span><span class="sxs-lookup"><span data-stu-id="93c30-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="93c30-116">Exempel 3: generera en signatur för signaturer som använder en delad åtkomst policy</span><span class="sxs-lookup"><span data-stu-id="93c30-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="93c30-117">Det här kommandot skapar ett signatur-token för delad åtkomst för lagrings resursen som heter ContosoShare och som har principen med namnet ContosoPolicy03.</span><span class="sxs-lookup"><span data-stu-id="93c30-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="93c30-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93c30-118">PARAMETERS</span></span>

### <span data-ttu-id="93c30-119">-Kontext</span><span class="sxs-lookup"><span data-stu-id="93c30-119">-Context</span></span>
<span data-ttu-id="93c30-120">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="93c30-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="93c30-121">Använd New-AzStorageContext cmdlet för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="93c30-121">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="93c30-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93c30-122">-DefaultProfile</span></span>
<span data-ttu-id="93c30-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="93c30-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93c30-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="93c30-124">-ExpiryTime</span></span>
<span data-ttu-id="93c30-125">Anger den tid då den delade åtkomst-signaturen blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="93c30-125">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="93c30-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="93c30-126">-FullUri</span></span>
<span data-ttu-id="93c30-127">Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="93c30-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="93c30-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="93c30-128">-IPAddressOrRange</span></span>
<span data-ttu-id="93c30-129">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="93c30-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="93c30-130">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="93c30-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="93c30-131">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="93c30-131">-Permission</span></span>
<span data-ttu-id="93c30-132">Anger behörigheterna i token för att komma åt resursen och filerna under resursen.</span><span class="sxs-lookup"><span data-stu-id="93c30-132">Specifies the permissions in the token to access the share and files under the share.</span></span>
<span data-ttu-id="93c30-133">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="93c30-133">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="93c30-134">-Princip</span><span class="sxs-lookup"><span data-stu-id="93c30-134">-Policy</span></span>
<span data-ttu-id="93c30-135">Anger den lagrade åtkomst principen för en resurs.</span><span class="sxs-lookup"><span data-stu-id="93c30-135">Specifies the stored access policy for a share.</span></span>

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

### <span data-ttu-id="93c30-136">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="93c30-136">-Protocol</span></span>
<span data-ttu-id="93c30-137">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="93c30-137">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="93c30-138">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="93c30-138">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="93c30-139">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="93c30-139">HttpsOnly</span></span>
* <span data-ttu-id="93c30-140">HttpsOrHttp standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="93c30-140">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="93c30-141">-ShareName</span><span class="sxs-lookup"><span data-stu-id="93c30-141">-ShareName</span></span>
<span data-ttu-id="93c30-142">Anger namnet på lagrings resursen.</span><span class="sxs-lookup"><span data-stu-id="93c30-142">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93c30-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="93c30-143">-StartTime</span></span>
<span data-ttu-id="93c30-144">Anger den tid då den delade Access-signaturen blir giltig.</span><span class="sxs-lookup"><span data-stu-id="93c30-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="93c30-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c30-145">CommonParameters</span></span>
<span data-ttu-id="93c30-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93c30-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c30-147">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93c30-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c30-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93c30-148">INPUTS</span></span>

### <span data-ttu-id="93c30-149">System. String</span><span class="sxs-lookup"><span data-stu-id="93c30-149">System.String</span></span>

### <span data-ttu-id="93c30-150">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="93c30-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="93c30-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93c30-151">OUTPUTS</span></span>

### <span data-ttu-id="93c30-152">System. String</span><span class="sxs-lookup"><span data-stu-id="93c30-152">System.String</span></span>

## <span data-ttu-id="93c30-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93c30-153">NOTES</span></span>
* <span data-ttu-id="93c30-154">Nyckelord: Allmänt, Azure, tjänster, data, lagring, BLOB, kö, tabell</span><span class="sxs-lookup"><span data-stu-id="93c30-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="93c30-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93c30-155">RELATED LINKS</span></span>

[<span data-ttu-id="93c30-156">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="93c30-156">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="93c30-157">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="93c30-157">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)
