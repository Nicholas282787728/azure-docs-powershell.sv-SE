---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 399c4030f9cd3efd04ec41ce3ab3475f0a660f4f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924657"
---
# <span data-ttu-id="de304-101">New-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="de304-101">New-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="de304-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de304-102">SYNOPSIS</span></span>
<span data-ttu-id="de304-103">Skapar nya autentiseringsuppgifter för ett Edge Storage-konto på enheten.</span><span class="sxs-lookup"><span data-stu-id="de304-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="de304-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de304-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de304-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de304-105">DESCRIPTION</span></span>
<span data-ttu-id="de304-106">**New-AzDataBoxEdgeStorageAccountCredential-** cmdleten skapar en ny autentiseringsuppgift för lagrings konto för en data box.</span><span class="sxs-lookup"><span data-stu-id="de304-106">The **New-AzDataBoxEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="de304-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de304-107">EXAMPLES</span></span>

### <span data-ttu-id="de304-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="de304-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="de304-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de304-109">PARAMETERS</span></span>

### <span data-ttu-id="de304-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de304-110">-AsJob</span></span>
<span data-ttu-id="de304-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="de304-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="de304-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de304-112">-DefaultProfile</span></span>
<span data-ttu-id="de304-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="de304-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de304-114">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="de304-114">-DeviceName</span></span>
<span data-ttu-id="de304-115">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="de304-115">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de304-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="de304-116">-EncryptionKey</span></span>
<span data-ttu-id="de304-117">Enhetens krypterings nycklar</span><span class="sxs-lookup"><span data-stu-id="de304-117">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de304-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="de304-118">-Name</span></span>
<span data-ttu-id="de304-119">Namn på det lagrings konto som ska användas</span><span class="sxs-lookup"><span data-stu-id="de304-119">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de304-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de304-120">-ResourceGroupName</span></span>
<span data-ttu-id="de304-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="de304-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de304-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="de304-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="de304-123">Ange åtkomst nycklar för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="de304-123">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de304-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="de304-124">-StorageAccountType</span></span>
<span data-ttu-id="de304-125">Möjlig lagrings åtkomst typ GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="de304-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="de304-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="de304-126">-Confirm</span></span>
<span data-ttu-id="de304-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="de304-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de304-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de304-128">-WhatIf</span></span>
<span data-ttu-id="de304-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="de304-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de304-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="de304-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de304-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de304-131">CommonParameters</span></span>
<span data-ttu-id="de304-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de304-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de304-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de304-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de304-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de304-134">INPUTS</span></span>

### <span data-ttu-id="de304-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="de304-135">None</span></span>

## <span data-ttu-id="de304-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de304-136">OUTPUTS</span></span>

### <span data-ttu-id="de304-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="de304-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="de304-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de304-138">NOTES</span></span>

## <span data-ttu-id="de304-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de304-139">RELATED LINKS</span></span>
