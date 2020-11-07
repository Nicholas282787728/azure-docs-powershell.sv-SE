---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7642F18A-B193-4849-BE3C-1B85FBD213F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 663ac3d8342e5ba231276e560408f8f7f6e74741
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758268"
---
# <span data-ttu-id="919ef-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="919ef-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="919ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="919ef-102">SYNOPSIS</span></span>
<span data-ttu-id="919ef-103">Anger ett Överlagrings valv för servern.</span><span class="sxs-lookup"><span data-stu-id="919ef-103">Sets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="919ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="919ef-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerBackupLongTermRetentionVault -ResourceId <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="919ef-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="919ef-105">DESCRIPTION</span></span>
<span data-ttu-id="919ef-106">Cmdleten **set-AzureRmSqlServerBackupLongTermRetentionVault** anger det långsiktiga bevarande valvet som är registrerat för den här servern.</span><span class="sxs-lookup"><span data-stu-id="919ef-106">The **Set-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet sets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="919ef-107">Valvet är en Azure Backup-resurs som används för att lagra säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="919ef-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="919ef-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="919ef-108">EXAMPLES</span></span>

## <span data-ttu-id="919ef-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="919ef-109">PARAMETERS</span></span>

### <span data-ttu-id="919ef-110">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="919ef-110">-ResourceGroupName</span></span>
<span data-ttu-id="919ef-111">Anger namnet på den resurs grupp som innehåller servern.</span><span class="sxs-lookup"><span data-stu-id="919ef-111">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="919ef-112">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="919ef-112">-ResourceId</span></span>
<span data-ttu-id="919ef-113">Anger ID för en resurs.</span><span class="sxs-lookup"><span data-stu-id="919ef-113">Specifies the ID of a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="919ef-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="919ef-114">-ServerName</span></span>
<span data-ttu-id="919ef-115">Anger den server som cmdleten ställer in ett valv för.</span><span class="sxs-lookup"><span data-stu-id="919ef-115">Specifies the server for which this cmdlet sets a vault.</span></span>

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

### <span data-ttu-id="919ef-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="919ef-116">-Confirm</span></span>
<span data-ttu-id="919ef-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="919ef-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919ef-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="919ef-118">-WhatIf</span></span>
<span data-ttu-id="919ef-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="919ef-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="919ef-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="919ef-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919ef-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="919ef-121">-DefaultProfile</span></span>
<span data-ttu-id="919ef-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="919ef-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="919ef-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="919ef-123">CommonParameters</span></span>
<span data-ttu-id="919ef-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="919ef-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="919ef-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="919ef-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="919ef-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="919ef-126">INPUTS</span></span>

## <span data-ttu-id="919ef-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="919ef-127">OUTPUTS</span></span>

## <span data-ttu-id="919ef-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="919ef-128">NOTES</span></span>

## <span data-ttu-id="919ef-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="919ef-129">RELATED LINKS</span></span>

[<span data-ttu-id="919ef-130">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="919ef-130">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Get-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="919ef-131">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="919ef-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
