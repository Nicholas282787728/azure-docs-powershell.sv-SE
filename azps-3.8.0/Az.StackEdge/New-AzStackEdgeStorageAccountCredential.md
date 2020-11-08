---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: d4e9062b15e7d5ca7338e13cdcdf71506ba23e29
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090785"
---
# <span data-ttu-id="2a632-101">New-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="2a632-101">New-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="2a632-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a632-102">SYNOPSIS</span></span>
<span data-ttu-id="2a632-103">Skapar nya autentiseringsuppgifter för ett Edge Storage-konto på enheten.</span><span class="sxs-lookup"><span data-stu-id="2a632-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="2a632-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a632-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a632-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a632-105">DESCRIPTION</span></span>
<span data-ttu-id="2a632-106">**New-AzStackEdgeStorageAccountCredential-** cmdleten skapar en ny autentiseringsuppgift för lagrings utrymme för en stack Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="2a632-106">The **New-AzStackEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="2a632-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a632-107">EXAMPLES</span></span>

### <span data-ttu-id="2a632-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2a632-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="2a632-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a632-109">PARAMETERS</span></span>

### <span data-ttu-id="2a632-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a632-110">-AsJob</span></span>
<span data-ttu-id="2a632-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2a632-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a632-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a632-112">-DefaultProfile</span></span>
<span data-ttu-id="2a632-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a632-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a632-114">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="2a632-114">-DeviceName</span></span>
<span data-ttu-id="2a632-115">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="2a632-115">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a632-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="2a632-116">-EncryptionKey</span></span>
<span data-ttu-id="2a632-117">Enhetens krypterings nycklar</span><span class="sxs-lookup"><span data-stu-id="2a632-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="2a632-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="2a632-118">-Name</span></span>
<span data-ttu-id="2a632-119">Namn på det lagrings konto som ska användas</span><span class="sxs-lookup"><span data-stu-id="2a632-119">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a632-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a632-120">-ResourceGroupName</span></span>
<span data-ttu-id="2a632-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="2a632-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a632-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="2a632-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="2a632-123">Ange åtkomst nycklar för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="2a632-123">provide storage account access key</span></span>

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

### <span data-ttu-id="2a632-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="2a632-124">-StorageAccountType</span></span>
<span data-ttu-id="2a632-125">Möjlig lagrings åtkomst typ GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="2a632-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="2a632-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2a632-126">-Confirm</span></span>
<span data-ttu-id="2a632-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2a632-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a632-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a632-128">-WhatIf</span></span>
<span data-ttu-id="2a632-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2a632-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a632-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2a632-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a632-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a632-131">CommonParameters</span></span>
<span data-ttu-id="2a632-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a632-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a632-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a632-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a632-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a632-134">INPUTS</span></span>

### <span data-ttu-id="2a632-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="2a632-135">None</span></span>

## <span data-ttu-id="2a632-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a632-136">OUTPUTS</span></span>

### <span data-ttu-id="2a632-137">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="2a632-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="2a632-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a632-138">NOTES</span></span>

## <span data-ttu-id="2a632-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a632-139">RELATED LINKS</span></span>
