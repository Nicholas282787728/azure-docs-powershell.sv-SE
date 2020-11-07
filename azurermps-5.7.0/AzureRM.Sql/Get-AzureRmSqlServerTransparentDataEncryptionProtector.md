---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: ecb49271c49e441140a43f8cb8ae5d65be56cd4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757182"
---
# <span data-ttu-id="e0cac-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e0cac-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="e0cac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0cac-102">SYNOPSIS</span></span>
<span data-ttu-id="e0cac-103">Hämtar skyddet för transparent data kryptering (TDE)</span><span class="sxs-lookup"><span data-stu-id="e0cac-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0cac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0cac-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0cac-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0cac-105">DESCRIPTION</span></span>
<span data-ttu-id="e0cac-106">Get-AzureRmSqlServerTransparentDataEncryptionProtector-cmdleten hämtar information om TDE-skydd.</span><span class="sxs-lookup"><span data-stu-id="e0cac-106">The Get-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="e0cac-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0cac-107">EXAMPLES</span></span>

### <span data-ttu-id="e0cac-108">Exempel 1: Hämta det transparenta data krypterings skyddet (TDE)</span><span class="sxs-lookup"><span data-stu-id="e0cac-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzureRmSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="e0cac-109">Det här kommandot får TDE-skyddet för servern som heter ContosoServer i resurs gruppen med namnet ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e0cac-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>

<span data-ttu-id="e0cac-110">ResourceGroupName ServerName ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="e0cac-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="e0cac-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="e0cac-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="e0cac-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0cac-112">PARAMETERS</span></span>

### <span data-ttu-id="e0cac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0cac-113">-DefaultProfile</span></span>
<span data-ttu-id="e0cac-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e0cac-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0cac-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0cac-115">-ResourceGroupName</span></span>
<span data-ttu-id="e0cac-116">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="e0cac-116">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0cac-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e0cac-117">-ServerName</span></span>
<span data-ttu-id="e0cac-118">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="e0cac-118">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0cac-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e0cac-119">-Confirm</span></span>
<span data-ttu-id="e0cac-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e0cac-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0cac-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0cac-121">-WhatIf</span></span>
<span data-ttu-id="e0cac-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e0cac-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0cac-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e0cac-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0cac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0cac-124">CommonParameters</span></span>
<span data-ttu-id="e0cac-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0cac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0cac-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0cac-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0cac-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0cac-127">INPUTS</span></span>

### <span data-ttu-id="e0cac-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e0cac-128">System.String</span></span>

## <span data-ttu-id="e0cac-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0cac-129">OUTPUTS</span></span>

### <span data-ttu-id="e0cac-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="e0cac-130">System.Object</span></span>

## <span data-ttu-id="e0cac-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0cac-131">NOTES</span></span>

## <span data-ttu-id="e0cac-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0cac-132">RELATED LINKS</span></span>

[<span data-ttu-id="e0cac-133">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="e0cac-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
